<template>
  <section>
    <section>
      <img
        src="@/assets/images/words-logo.png"
        alt=""
        width="200"
        style="border-radius: 50%"
      />
      <p>Just Words</p>
    </section>

    <section>
      <p class="p_row">
        <img src="@/assets/images/taro-logo.png" alt="" />
        <span>+</span>
        <img src="@/assets/images/tengxun-cloud.svg" alt="" />
      </p>
    </section>

    <section>
      <div class="words-imgs">
        <img src="@/assets/images/project-01-01.png" alt="" />
        <img src="@/assets/images/project-01-02.png" alt="" />
        <img src="@/assets/images/project-01-03.png" alt="" />
      </div>
    </section>
  </section>
</template>

<style scoped>
.words-imgs {
  display: flex;
  justify-content: space-between;
}
.words-imgs img {
  width: 25%;
}

.p_row {
  display: flex;
  align-items: center;
  justify-content: center;
}

.p_row img {
  height: 40px;
}

.p_row span {
  margin: 0 50px;
}
</style>
