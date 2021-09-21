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
        <span id="copied-message" v-show="showMessage">{{ message }}</span>
        <button id="btn-copy" class="btn btn-primary" @click="copyPassword()">
            Copy
        </button>
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
            message: '',
            showMessage: false,
        }
    },
    methods: {
        renderCode(): void {
            this.currentPassword = generatePass()
        },
        copyPassword(): void {
            let password = navigator.clipboard.writeText(this.currentPassword)
            password
                .then(() => {
                    console.log('Password copied to the clipboard')
                    this.message = 'Password copied to the clipboard'
                    this.showMessage = true
                })
                .catch((e) => {
                    console.error(e)
                    this.message =
                        'An Error happened. Password was not copied to the clipboard'
                })
        },
    },
})
</script>

<style lang="scss">
@use 'box-style';
</style>
