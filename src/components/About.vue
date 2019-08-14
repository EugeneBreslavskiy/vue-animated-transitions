<template>
  <section class="section">
    <div class="img-wrapper">
      <span class="img-curtain img-about-curtain"></span>
      <img src="../assets/about.jpg">
    </div>
    <h1 class="header-about">
      <span class="header-letter-wrapper">
        <span class="header-letter">
          f
        </span>
      </span>
      <span class="header-letter-wrapper">
        <span class="header-letter">
          a
        </span>
      </span>
      <span class="header-letter-wrapper">
        <span class="header-letter">
          c
        </span>
      </span>
      <span class="header-letter-wrapper">
        <span class="header-letter">
          t
        </span>
      </span>
      <span class="header-letter-wrapper">
        <span class="header-letter">
          o
        </span>
      </span>
      <span class="header-letter-wrapper">
        <span class="header-letter">
          r
        </span>
      </span>
    </h1>
    <div class="text-about-wrapper">
      <p class="text-about">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Blanditiis dolores nulla tempora velit! Animi, magnam! Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
      </p>
      <p class="text-about">
        Ad aliquid animi asperiores beatae consequuntur culpa cum delectus deserunt dolore et facere illum impedit ipsum laboriosam minima nam obcaecati optio possimus quaerat quo, reiciendis sunt suscipit unde velit vero voluptatem voluptatum?
      </p>
      <p class="text-about">
        Aperiam architecto at dignissimos enim expedita fugiat, id impedit maxime neque nobis sunt, suscipit, tempore unde. Commodi.
      </p>
    </div>
  </section>
</template>

<script>
    export default {
        name: "About"
    }
</script>

<style lang="sass">
  
  .header-about
    position: absolute
    top: 20%
    left: 34px
  
  .text-about-wrapper
    max-width: 400px
    position: absolute
    left: 45px
  
  .text-about
    margin: 15px 0

</style>
