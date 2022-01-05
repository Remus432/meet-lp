<script>
  import Description from "./Description.svelte"
</script>

<section class="hero">
  <nav class="hero__nav">
    <img src="/assets/logo.svg" alt="Meet Logo" class="hero__logo">
  </nav>
  <div class="hero__showcase">
    <img src="/assets/desktop/image-hero-left.png" alt="" class="hero__avatars-left">
    <img src="/assets/tablet/image-hero.png" alt="User Avatars" class="hero__avatars">
    <Description />
    <img src="/assets/desktop/image-hero-right.png" alt="" class="hero__avatars-right">
  </div>
</section>

<style lang="scss">
  @import "../styles/variables";
  @import "../styles/mixins";

  .hero {
    padding: 0 $spacing-s;
    text-align: center;

    &__nav {
      margin-bottom: 5.4rem;
    }
    
    &__avatars {
      margin-bottom: 4.8rem;
      transform: scale(1.3);
      width: 100%;

      &-left,
      &-right {
        display: none;
      }
    }

    @include respond(tab) {
      padding: 0 $spacing-l;

      &__nav {
        margin-bottom: $spacing-xxl;
      }

      &__avatars {
        margin-bottom: 7.2rem;
        transform: scale(1.2);
      }
    }

    @include respond(desktop) {
      padding: 0;

      &__showcase {
        align-items: center;
        display: flex;
        justify-content: space-between;
        width: 100%;
      }

      &__avatars {
        display: none;

        &-left,
        &-right {
          display: unset;
          position: relative;
        }

        &-left {
          left: -2.5vw;
        }

        &-right {
          right: -2.5vw;
        }
      }
    }
  }
</style>