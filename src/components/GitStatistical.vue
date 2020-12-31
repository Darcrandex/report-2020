<template>
  <section>
    <section>Projects Git <b class="mark">Statistical</b></section>

    <section data-auto-animate>
      <p class="mark">Commits</p>
      <div v-for="item in commitsData" :key="item.labelId">
        <span :data-id="item.labelId" class="row-label">{{ item.label }}</span>
        <div
          :data-id="item.progressId"
          class="row-progress"
          style="width: 0px; background: rgba(0, 0, 0, 0)"
        ></div>
        <span :data-id="item.dataId" class="row-value" style="opacity: 0"
          >{{ item.commits }} commit</span
        >
      </div>
    </section>

    <section data-auto-animate>
      <p class="mark">Commits</p>
      <div v-for="item in commitsData" :key="item.labelId">
        <span :data-id="item.labelId" class="row-label">{{ item.label }}</span>
        <div
          :data-id="item.progressId"
          class="row-progress"
          :style="{
            width: '50%',
            background: `linear-gradient(to right, ${item.color}, ${item.color} ${item.percent}, rgba(0,0,0,0) ${item.percent})`,
          }"
        ></div>
        <span :data-id="item.dataId" class="row-value" style="opacity: 1"
          >{{ item.commits }} commit</span
        >
      </div>
    </section>

    <section data-auto-animate>
      <p class="mark">Added Lines</p>
      <div v-for="item in addedLinesData" :key="item.labelId">
        <span :data-id="item.labelId" class="row-label">{{ item.label }}</span>
        <div
          :data-id="item.progressId"
          class="row-progress"
          style="width: 0px; background: rgba(0, 0, 0, 0)"
        ></div>
        <span :data-id="item.dataId" class="row-value" style="opacity: 0"
          >{{ item.addedLines }} lines</span
        >
      </div>
    </section>

    <section data-auto-animate>
      <p class="mark">Added Lines</p>
      <div v-for="item in addedLinesData" :key="item.labelId">
        <span :data-id="item.labelId" class="row-label">{{ item.label }}</span>
        <div
          :data-id="item.progressId"
          class="row-progress"
          :style="{
            width: '50%',
            background: `linear-gradient(to right, ${item.color}, ${item.color} ${item.percent}, rgba(0,0,0,0) ${item.percent})`,
          }"
        ></div>
        <span :data-id="item.dataId" class="row-value" style="opacity: 1"
          >{{ item.addedLines }} lines</span
        >
      </div>
    </section>

    <section>
      <img src="@/assets/images/project-edu-01.png" alt="" />
    </section>
    <section>
      <img src="@/assets/images/project-edu-02.png" alt="" />
    </section>
    <section>
      <img src="@/assets/images/project-edu-03.png" alt="" />
    </section>
  </section>
</template>

<script>
const colors = [
  "#49a942",
  "#fe5000",
  "#74d2e7",
  "#a0ac48",
  "#2e9df7",
  "#b9dca4",
];
export default {
  // 原始数据
  data: () => ({
    list: [
      { label: "edu pc", commits: 6162, addedLines: 4395284 },
      { label: "party construction", commits: 31, addedLines: 114678 },
      { label: "edu h5", commits: 47, addedLines: 3110 },
      { label: "edu website ssr", commits: 64, addedLines: 71638 },
      { label: "edu website admin", commits: 156, addedLines: 80154 },
      { label: "edu taro", commits: 54, addedLines: 92902 },
    ],
  }),

  computed: {
    commitsData() {
      const max = Math.max(...this.list.map((v) => v.commits));
      const res = this.list.map((v, i) => ({
        ...v,
        labelId: `commit_row_${i}_label`,
        progressId: `commit_row_${i}_p`,
        dataId: `commit_row_${i}_data`,

        // 2x 是为了让数据看起来差距没有那么大
        percent: `${(2 * 100 * (v.commits / max)).toFixed(2)}%`,
        color: colors[i],
      }));
      return res;
    },
    addedLinesData() {
      const max = Math.max(...this.list.map((v) => v.addedLines));
      const res = this.list.map((v, i) => ({
        ...v,
        labelId: `added_lines_row_${i}_label`,
        progressId: `added_lines_row_${i}_p`,
        dataId: `added_lines_row_${i}_data`,

        // 2x 是为了让数据看起来差距没有那么大
        percent: `${(2 * 100 * (v.addedLines / max)).toFixed(2)}%`,
        color: colors[i],
      }));
      return res;
    },
  },
};
</script>

<style>
.row-label {
  display: inline-block;
  width: 10em;
  font-size: 24px;
  text-align: right;
}

.row-progress {
  display: inline-block;
  height: 10px;
  margin: 0 10px;
}

.row-value {
  display: inline-block;
  width: 8em;
  font-size: 16px;
  text-align: left;
  font-weight: normal;
  font-style: italic;
}
</style>