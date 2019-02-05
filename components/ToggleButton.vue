<template>
    <div class="button" @click="emit('toggle')">
        <div class="button-inner" :style="'box-shadow:' + toggleButtonBoxShadow + ';'">
            <div class="button-toggle" :style="'left:' + togglePosition + 'px' + '; background-color:' + toggleButtonColor + ';'"></div>
        </div>
    </div>
</template>

<script>

    export default {
        name: 'ToggleButton',
        components: {},
        props: ['toggleButtonColor', 'toggleButtonBoxShadow', 'togglePosition'],
        data() {
            return {

            }
        },
        methods: {
            emit(param) {
                this.$emit(param)
            }
        }
    }
</script>

<style>
    .button {
        cursor: pointer;
        /* position: absolute; */
        /* top: 20px; */
        /* left: 20px; */
        /* border: 1px solid rgba(169, 169, 169, 0.5); */
        /* width: 46px; */
        /* height: 28px; */
        border-radius: 15px;
        /* display: flex; */
        /* justify-content: center; */
        /* align-items: center; */
        margin-right: 28px;
        margin-left: 28px;
    }

    .button-inner {
        cursor: pointer;
        position: relative;
        width: 42px;
        height: 24px;
        border: 1px solid #2e2e2e;
        border-radius: 15px;
        display: flex;
        align-items: center;
        /*background-color: #D3D3D3;*/
        transition: all 400ms;
        box-shadow: 1px 1px 1px #D3D3D3;
    }

    .button-toggle {
        cursor: pointer;
        position: absolute;
        width: 20px;
        height: 20px;
        top: 1px;
        border: 1px solid #2e2e2e;
        /*box-shadow: 1px 1px 1px rgb(175, 173, 173);*/
        border-radius: 15px;
        transition: all 200ms;
    }
</style>
