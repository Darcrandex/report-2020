<template>
  <section>
    <section>
      <img
        src="@/assets/images/afaire-logo.jpg"
        alt=""
        width="200"
        style="background-color: #ffffff"
      />
      <p>Afaire</p>
    </section>

    <section>
      <p class="p_row">
        <img src="@/assets/images/react-logo.svg" alt="" />
        <span>+</span>
        <img src="@/assets/images/nodejs_logo.svg" alt="" />
        <span>+</span>
        <img src="@/assets/images/mongodb.png" alt="" />
      </p>
    </section>

    <section>
      <img src="@/assets/images/project-02-01.png" alt="" />
    </section>
    <section>
      <img src="@/assets/images/project-02-02.png" alt="" />
    </section>
    <section>
      <img src="@/assets/images/project-02-03.png" alt="" />
    </section>
  </section>
</template>

<style scoped>
.p_row {
  display: flex;
  align-items: center;
  justify-content: center;
}

.p_row img {
  height: 70px;
}

.p_row span {
  margin: 0 40px;
}
</style>
