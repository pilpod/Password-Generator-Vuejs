<template>
    <div>
        <form-generator></form-generator>
        <box-to-paste></box-to-paste>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'
import FormGeneratorVue from './components/genetator/FormGenerator.vue'
import BoxToPasteMessageVue from './components/boxToPasteMessage/BoxToPasteMessage.vue'

export default Vue.extend({
    name: 'App',
    data: function () {
        return {
            title: 'Password Generator'
        }
    },
    components: {
        'form-generator': FormGeneratorVue,
        'box-to-paste': BoxToPasteMessageVue,
    },
})
</script>

<style lang="scss">
@use 'styles';
</style>
