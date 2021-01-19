<template>
  <section>
    <section>
      <div class="video-title">
        <img src="@/assets/images/css-logo.jpg" alt="" width="98" />
        <span class="video-plus">+</span>
        <img src="@/assets/images/premiere-logo.png" alt="" width="100" />
      </div>
    </section>

    <section>
      <video data-autoplay src="@/assets/media/react-logo.mp4"></video>
    </section>
    <section>
      <video data-autoplay src="@/assets/media/word-chop.mp4"></video>
    </section>
  </section>
</template>

<style>
.video-title {
  display: flex;
  align-items: center;
  justify-content: center;
}

.video-plus {
  margin: 0 20px;
  font-size: 200%;
}
</style>
