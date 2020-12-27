<template>
  <div class="reveal">
    <div class="slides">
      <section>hello</section>
      <section>world</section>
      <GitStatistical />

      <section>
        <h2>My Projects</h2>
        <ul>
          <li>Just Words</li>
          <li>Afaire</li>
          <li>CSS + Premiere</li>
          <li>Vuepress Blog</li>
        </ul>
      </section>

      <Words />
      <Afaire />
      <Video />
      <Blog />
    </div>
  </div>
</template>

<script>
import { nextTick } from "vue";
import Reveal from "reveal.js";

import GitStatistical from "./components/GitStatistical.vue";
import Words from "./components/Words.vue";
import Afaire from "./components/Afaire.vue";
import Video from "./components/Video.vue";
import Blog from "./components/Blog.vue";

export default {
  name: "App",
  components: { GitStatistical, Words, Afaire, Blog, Video },
  setup() {
    nextTick(() => {
      Reveal.initialize({
        hash: true,
        progress: false,
      });
    });
  },
};
</script>

<style>
/* 需要加载 reveal.js 的主题样式 */
@import "../node_modules/reveal.js/dist/reset.css";
@import "../node_modules/reveal.js/dist/reveal.css";
@import "../node_modules/reveal.js/dist/theme/black.css";

#app {
  height: 100%;
}
</style>
