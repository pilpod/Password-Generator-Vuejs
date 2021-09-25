<template>
    <div class="box">
        <input
            id="input-editable"
            class="form-control"
            contenteditable="text"
            type="text"
            placeholder="Paste the Code here"
        />
        <p>{{ message }}</p>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
    name: 'BoxToPasteMessage',
    data() {
        return {
            message: 'Box to paste message'
        }
    },
})
</script>


<style lang="scss">
@use '../../sass/box-style';
@use '../../sass/input-style.scss';
</style>
