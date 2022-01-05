<script>
  export let count
</script>

<div class="counter counter--{count}">
  <div class="counter__line"></div>
  <div class="counter__value">0{count}</div>
</div>

<style lang="scss">
  @import "../styles/variables";
  @import "../styles/mixins";

  .counter {
    flex-direction: column;
    margin: $spacing-xxl 0;

    &--2 {
      transform: translateY(calc(($spacing-xxl * 150) / 100));
      transform-origin: bottom;
    }

    @include flexCenter;

    &__line {
      background-color: rgba($secondary-text-color, .25);
      height: 8.4rem;
      width: .1rem;
    }

    &__value {
      background-color: $bg-color;
      border: 1px solid rgba($secondary-text-color, .25);
      border-radius: 50%;
      color: $secondary-text-color;
      font-size: $font-xs;
      font-weight: 900;
      height: 5.6rem;
      width: 5.6rem;

      @include flexCenter;
    }

    @include respond(tab) {
      margin-top: 8rem;
    }
  }
</style>