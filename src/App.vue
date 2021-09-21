<template>
    <div>
        <FormGenerator />
    </div>
</template>

<script lang="ts">
import Vue from 'vue'
import FormGeneratorVue from './components/genetator/FormGenerator.vue'

export default Vue.extend({
    name: 'App',
    data: function () {
        return {
            title: 'Password Generator',
        }
    },
    components: {
        FormGenerator: FormGeneratorVue,
    },
})
</script>

<style lang="scss">
@use 'styles';
</style>
