<template>
    <div :class="data.class">
        <app-article-preview :dataItem="data.element_item.list_items" />
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
.whats-new  {
  grid-template-columns: 1fr 2fr 1fr;
  grid-template-rows: auto;
  grid-column-gap: 42px;
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
    grid-row-start: 1;
    grid-column-start: 4;
  }
  &__item5 {
    grid-row-start: 3;
    grid-column-start: 1;
  }
  &__item6 {
    grid-row-start: 4;
    grid-column-start: 2;
  }
  &__item7 {
    grid-row-start: 4;
    grid-column: 3 / -1;
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