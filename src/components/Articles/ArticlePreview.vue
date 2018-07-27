<template>
    <div>
        <div v-for="(item,index) in listItem" :key="index" class="whats-newitem1">
            <img :src="item.imgUrl" alt="">
            <h1>
                {{ item.title }}
            </h1>
            <p> {{ item.content }} </p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppArticlePreview',
        props: {
            listItem: Array,
            required: true
        }
        
    }
</script>

<style scoped lang="scss">
img { 
    width: 100%
    } 
</style>