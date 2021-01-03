<template>
  <div class="reveal">
    <div class="slides">
      <section>
        <p>Year-end Summary For <b class="mark">2020</b></p>
        <p class="author">by Darcrand🐞</p>
      </section>

      <Description />
      <GitStatistical />
      <SkillExtension />

      <section>
        <p>My <b class="mark">Personal</b> Projects</p>
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
      <Ending />
    </div>
  </div>
</template>

<script>
import { nextTick } from "vue";
import Reveal from "reveal.js";

import Description from "./components/Description.vue";
import GitStatistical from "./components/GitStatistical.vue";
import SkillExtension from "./components/SkillExtension.vue";
import Words from "./components/Words.vue";
import Afaire from "./components/Afaire.vue";
import Video from "./components/Video.vue";
import Blog from "./components/Blog.vue";
import Ending from "./components/Ending.vue";

export default {
  name: "App",
  components: {
    Description,
    GitStatistical,
    SkillExtension,
    Words,
    Afaire,
    Blog,
    Video,
    Ending,
  },
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

.mark {
  font-weight: bold;
  color: #42b983;
}

.author {
  font-size: 18px;
}
</style>
