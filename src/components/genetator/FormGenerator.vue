<template>
    <div class="box">
        <h2 id="title">{{ title }}</h2>
        <input
            id="input-pass"
            class="form-control input-pass"
            type="text"
            name="randomPassword"
            placeholder="password"
            :value="currentPassword"
        />
        <button id="btn-copy" class="btn btn-primary">Copy</button>
        <button id="btn-generate" class="btn btn-primary" @click="renderCode()">
            Generate
        </button>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'
import generatePass from '../modules/generator'

export default Vue.extend({
    name: 'FormGenerator',
    data() {
        return {
            title: 'Password Generator',
            currentPassword: '',
        }
    },
    methods: {
        renderCode(): void {
            this.currentPassword = generatePass()
        },
    },
})
</script>

<style lang="scss">
@use 'box-style';
</style>
