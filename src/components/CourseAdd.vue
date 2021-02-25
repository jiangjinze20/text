<template>
    <div>
        <input  :value="value" @input="onInput" @keydown.enter="addCourse"/>
        <button v-on:click="addCourse">新增课程</button>
    </div>
</template>

<script>
export default {
    name: "courseAdd",
    props: ['value'],
    methods: {
        addCourse() {
            this.$emit('add-course') ;
        },
        onInput(e) {
            this.$emit('input', e.target.value)
        }
    }
}
</script>

<style scoped>

</style>
