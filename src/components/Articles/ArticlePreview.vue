<template>
    <div>
        <div v-for="(item,index) in dataItem" :key="index" class="whats-newitem1">
            <img :src="item.id" alt="item">
            <h1>
                {{ item.title }}
            </h1>
            <p> </p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppArticlePreview',
        props: {
            dataItem: Array,
            required: true
        }
        
    }
</script>

<style scoped lang="scss">
img { 
    width: 100%
    } 
</style>