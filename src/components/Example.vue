<template>
    <div>
        <h1>{{ title }}</h1>
    </div>
</template>

<script lang="ts">
    import Vue from 'vue'
    export default Vue.extend({
        name: 'Example',
        data() {
            return {
                title: 'My first component'
            }
        },
    })
</script>