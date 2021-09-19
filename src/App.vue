<template>
  <div>
    <h1>
      {{ name }}
    </h1>
    <example></example>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Example from "./components/Example.vue";

export default Vue.extend({
  name: 'App',
  data: function () {
    return {
      name: "Hello Vue!",
    };
  },
  components: {
    'example': Example,
  },
});
</script>

<style lang="scss">
  @use "styles";
</style>
