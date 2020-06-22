<template>
    <div class="SYN1">
        <h1>{{ msg }}</h1>
        <form>
            输入：<input type='text' v-model="inputSyn2">
            同步：<input type='text' v-model="inputSyn2">
        </form>
    </div>
</template>

<script>
export default {
    name:'InputSyn2',
    data() {
        return {
            inputSyn2:'',
        }
    },
}
</script>