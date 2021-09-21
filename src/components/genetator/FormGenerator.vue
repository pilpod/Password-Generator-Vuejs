<template>
    <div class="box">
        <h1>{{ title }}</h1>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
    name: 'FormGenerator',
    data() {
        return {
            title: 'Password Generator'
        }
    },
})
</script>

<style lang="scss">
    @use 'box-style';
</style>