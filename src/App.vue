<template>
  <div id="app">
    <header class="header">
      <router-link to="/" class="logo">Factor</router-link>
      <router-link to="/about" class="link">About</router-link>
    </header>
    <transition :name="transition" mode="out-in">
      <router-view/>
    </transition>
  </div>
</template>

<script>
    export default {
        name: 'App',
        data() {
            return {
                transition: 'transition-in'
            }
        },
        watch: {
            '$route' (to, from) {
                
                const toDepth = to.path.length
                const fromDepth = from.path.length
                this.transition = toDepth > fromDepth ? 'transition-in' : 'transition-out'
                
            }
        }
    }
</script>

<style lang="sass">
  
  @import url('https://fonts.googleapis.com/css?family=Titillium+Web:300,400,700&display=swap')
  
  body
    margin: 0
    font-family: 'Titillium Web', sans-serif
    font-size: 14px
    font-weight: 300
    font-style: normal
    font-stretch: normal
    line-height: 24px
    
    h1
      display: flex
      justify-content: center
      margin: 0
      font-size: 90px
      line-height: 110px
      text-align: center
      text-transform: uppercase
    
    a
      color: #000
      text-decoration: none
      transition: 0.5s ease
      &:hover
        color: #979797
      
      &.logo
        font-size: 16px
        font-weight: 700
        
      &.link-twitter
        position: absolute
        right: 40px
        bottom: 40px
        
      &.link-facebook
        position: absolute
        left: 40px
        bottom: 40px
    
    img
      display: block
      width: 100%

  .header
    display: flex
    align-items: center
    justify-content: space-between
    padding: 40px
    position: absolute
    top: 0
    right: 0
    left: 0
    z-index: 5

  .section
    display: flex
    align-items: center
    justify-content: center
    min-height: 100vh
    overflow: hidden
    
  .img-wrapper
    width: 400px
    position: absolute
    overflow: hidden
    z-index: -1
    
  .img-curtain
    position: absolute
    top: 0
    right: 0
    bottom: 0
    left: 0
    background-color: #fff
    
    &.img-main-curtain
      transform: translate(-100%, 0%)
  
    &.img-about-curtain
      transform: translate(-100%, 0%)
  
  .header-letter-wrapper
    margin: 0 5px
    overflow: hidden
  
  .header-letter
    display: inline-block
  
  .transition-in-leave-active
    transition: 1s
  
    .img-curtain
      animation: slideOut 1s cubic-bezier(.77, 0, .175, 1)
  
    .header-letter
      animation: headerOut 1s cubic-bezier(.77, 0, .175, 1)
  
    .link-bottom
      animation: fadeOut 1s cubic-bezier(.77, 0, .175, 1)
      
  .transition-in-leave-to
    opacity: 0

  .transition-in-enter-active
    transition: 1s
  
    .img-curtain
      animation: slideIn 1s cubic-bezier(.77, 0, .175, 1)
  
    .header-letter
      animation: headerIn 1s cubic-bezier(.77, 0, .175, 1)
      
    .text-about
      animation: fadeIn 1s cubic-bezier(.77, 0, .175, 1)
      
  .transition-out-leave-active
    transition: 1s
    
    .img-curtain
      animation: slideOut 1s cubic-bezier(.77, 0, .175, 1)
  
    .header-letter
      animation: headerOut 1s cubic-bezier(.77, 0, .175, 1)
  
    .link-bottom
      animation: fadeOut 1s cubic-bezier(.77, 0, .175, 1)
      
    .text-about
      animation: fadeOut 1s cubic-bezier(.77, 0, .175, 1)
      
  .transition-out-leave-to
    opacity: 0
    
  .transition-out-enter-active
    transition: 1s
  
    .img-curtain
      animation: slideIn 1s cubic-bezier(.77, 0, .175, 1)
  
    .header-letter
      animation: headerIn 1s cubic-bezier(.77, 0, .175, 1)
  
    .link-bottom
      animation: fadeIn 1s cubic-bezier(.77, 0, .175, 1)
      
  @keyframes headerOut
    from
      transform: translate(0%, 0%)
    to
      transform: translate(100%, 0%)
    
  @keyframes headerIn
    from
      transform: translate(100%, 0%)
    to
      transform: translate(0%, 0%)
  
  @keyframes slideOut
    from
      transform: translate(-100%, 0%)
    to
      transform: translate(0%, 0%)
  
  @keyframes slideIn
    from
      transform: translate(0%, 0%)
    to
      transform: translate(-100%, 0%)
  
  @keyframes fadeOut
    from
      opacity: 1
    to
      opacity: 0
  
  @keyframes fadeIn
    from
      opacity: 0
    to
      opacity: 1
  
</style>
