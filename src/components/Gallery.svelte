<div class="gallery">
  <img src="/assets/desktop/image-woman-in-videocall.jpg" alt="Woman In Video Call" class="gallery__img">
  <img src="/assets/desktop/image-women-videochatting.jpg" alt="Women Videochatting" class="gallery__img">
  <img src="/assets/desktop/image-men-in-meeting.jpg" alt="Men In Meeting" class="gallery__img">
  <img src="/assets/desktop/image-man-texting.jpg" alt="Man Texting" class="gallery__img">
</div>

<style lang="scss">
  @import "../styles/variables";
  @import "../styles/mixins";

  .gallery {
    display: grid;
    gap: $spacing-s;
    grid-template-columns: repeat(2, 1fr);
    justify-items: center;

    &__img {
      border-radius: .8rem;
      width: 100%;
    }

    @include respond(tab) {
      gap: .7rem;
      grid-template-columns: repeat(4, 1fr);
    }
  }
</style>