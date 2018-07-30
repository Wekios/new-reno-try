<template>
    <div>
        <h1>  {{ data.class }} </h1>
    </div>
</template>

<script>
    export default {
        name: 'TestComponent',
        props: {
            data: Object,
            required: true
        }
    }
</script>

<style scoped lang="scss">
* {
    background-color: pink;
    color: orange;
}
</style>