<template>
  <section>
    <section>
      <div class="card">
        <img src="@/assets/images/steve-jobs.jpg" alt="" class="img" />
        <div class="content">
          <p>Stay hungry. Stay foolish.</p>
          <p class="author">Steve Jobs</p>
        </div>
      </div>
    </section>
    <section>
      <p>🎉 We refuel together.</p>
      <p class="mark">In 2021</p>
    </section>
  </section>
</template>

<style scoped>
.card {
  display: flex;
  align-items: center;
  justify-content: center;
}

.card .img {
  width: 200px;
}

.content {
  margin-left: 50px;
  text-align: right;
}

.author {
  font-style: italic;
}
</style>
