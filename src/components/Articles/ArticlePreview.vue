<template>
    <div :class="'item' + dataItem.id">
        <img 
            :src="dataItem.featured_image[0].data.file.url"
            :alt="dataItem.featured_image[0].data.seoname"
            >
        <h4>{{ dataItem.featured_image[0].data.caption }}</h4>
    </div>
</template>

<script>
export default {
  name: "AppArticlePreview",
  props: {
    dataItem: Object,
    required: true
  }
};
</script>

<style scoped lang="scss">
img {
  width: 100%;
  height: 100%;
}
</style>