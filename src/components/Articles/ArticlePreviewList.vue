<template>
  <div class="grid-list" :class="data.class">
    <app-article-preview v-for="dataItem in data.element_item.list_items" :key="dataItem.id" :dataItem="dataItem" />
  </div>
</template>

<script>
import AppArticlePreview from "./ArticlePreview.vue";
export default {
  name: "articlePreviewList",
  props: {
    data: Object,
    requred: true
  },
  components: {
    AppArticlePreview
  },
  computed: {
    // layoutPicker() {
    // Pick class for layout
    // }
  }
};
</script>

<style lang="scss">
.grid-list {
  display: grid;
  text-align: left;
  > div {
    position: relative;
    top: 0;
    cursor: pointer;
    transition: all 0.3s ease;
    &:hover {
      top: -10px;
    }
  }
}
.layout1 {
  grid-template-columns: 1fr 2fr 3fr;
  // grid-template-rows: 136px 456px 272px;
  grid-template-rows: auto;
  align-items: baseline;
  grid-column-gap: 32px;
  grid-row-gap: 0;
  &__title {
    grid-column: 1;
  }
  .item1 {
    grid-row-start: 1;
    grid-column-start: 1;
    align-self: baseline;
    // height: 264px;
  }

  .item2 {
    grid-row-start: 1;
    grid-column-start: 2;
    align-self: baseline;
    // height: 456px;
  }

  .item3 {
    grid-row-start: 1;
    grid-column-start: 3;
    // height: 400px;
  }

  .item4 {
    grid-row-start: 2;
    grid-column-start: 3;
    // height: 224px;
    img {
      width: 50%;
    }
  }
}

.my-business {
  grid-template-columns: repeat(3, 27.2rem) 1fr;
  grid-template-rows: 17.6rem 36rem;
  grid-column-gap: 3.2rem;
  grid-row-gap: 0;
  &__title {
    grid-column: 1;
  }
  &__item1 {
    grid-row-start: 2;
    grid-column-start: 1;
  }
  &__item2 {
    grid-row-start: 2;
    grid-column-start: 2;
  }
  &__item3 {
    grid-row-start: 1;
    grid-column-start: 3;
  }
  &__item4 {
    grid-row-start: 3;
    grid-column-start: 2;
  }
  &__item5 {
    grid-row-start: 3;
    grid-column-start: 3;
    grid-column-end: 3;
  }
}
</style>