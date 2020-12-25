<template>
  <section>
    <section>
      <img src="@/assets/images/vue-press-logo.png" alt="" width="200" />
      <p>Vuepress Blog</p>
    </section>

    <section>
      <div class="blog-code-container">
        <div class="top-circle">
          <span style="background-color: #ff5f56"></span>
          <span style="background-color: #ffbd2e"></span>
          <span style="background-color: #27c93f"></span>
        </div>
        <div class="fragment fade-up">
          <code class="red">cd </code>
          <code class="gray">src </code>
          <code class="blue">&& </code>
          <code class="gray">touch a.</code>
          <code class="red">md</code>
        </div>
        <div class="fragment fade-up">
          <code class="red">echo </code>
          <code class="green">'# A title here' </code>
          <code class="blue">> </code>
          <code class="gray">a.</code>
          <code class="red">md</code>
        </div>
        <div class="fragment fade-up">
          <code class="gray">yarn build</code>
        </div>
        <div class="fragment fade-up">
          <code class="gray">explorer https://darcrandex.github.io</code>
        </div>
      </div>
    </section>

    <section>
      <img src="@/assets/images/project-03-01.png" alt="" />
    </section>
  </section>
</template>

<style>
.blog-code-container {
  width: 80%;
  margin: 0 auto;
  padding: 25px;
  background-color: #282c34;
  border-radius: 10px;
  box-shadow: 0 0 30px 0 #000;

  text-align: left;
  font-family: Hack, monospace;
  font-size: 26px;
}

.top-circle {
  height: 15px;
  margin-bottom: 20px;
  line-height: 15px;
  font-size: 0;
}

.top-circle span {
  display: inline-block;
  margin-right: 10px;
  width: 15px;
  height: 15px;
  border-radius: 50%;
}

.blog-code-container .fragment {
  margin-bottom: 5px;
}

code.red {
  color: #e06c75;
}

code.green {
  color: #98c379;
}

code.blue {
  color: #56b6c2;
}

code.gray {
  color: #abb2bf;
}
</style>