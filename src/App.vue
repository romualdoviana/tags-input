<script>
export default {
  data: () => ({
    jsFrameworks: ["vue", "react", "angular"],
    backendFrameworks: ["Laravel"],
  }),

  methods: {
    handleChange(tags) {
      this.jsFrameworks = [...tags];
    },
  },
};
</script>

<template>
  <h1>Your favorite frameworks</h1>

  <div>{{ jsFrameworks }}</div>

  <tags-input :selected-tags="jsFrameworks" @change="handleChange" />

  <div>{{ backendFrameworks }}</div>

  <tags-input
    :selected-tags="backendFrameworks"
    @change="backendFrameworks = [...$event]"
  />
</template>

<style>
#app {
  max-width: 1280px;
  /* margin: 0 auto; */
  /* padding: 2rem; */
  font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: rgba(5, 5, 5, 0.87);
  margin-top: 60px;
}
h1 {
  color: blue;
}
</style>
