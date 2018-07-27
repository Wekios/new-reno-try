<template>
  <div class="home">
    <!-- <HeaderSlider img="https://picsum.photos/1440/700"/> -->
    <app-article-preview-list :list="list"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Navigation from "@/components/Navigation/Navigation.vue";
import HeaderSlider from "@/components/Header/HeaderSlider.vue";
import AppArticlePreviewList from '@/components/Articles/ArticlePreviewList';

export default {
  name: "home",
  data() {
    return {
      list: {
        whatsNew: {
          listTitle: "What's new",
          tag: 'whats-new',
          data: [
            { 
              title: 'hello',
              imgUrl: 'https://picsum.photos/200/300/?random',
              content: 'Lorem ipsum dummy content blah blah hello guys' 
            },
            { 
              title: 'hello 2',
              imgUrl: 'https://picsum.photos/200/300/?random',
              content: 'Lorem ipsum dummy content blah blah hello guys' 
            },
            { 
              title: 'hello 3',
              imgUrl: 'https://picsum.photos/200/300/?random',
              content: 'Lorem ipsum dummy content blah blah hello guys' 
            },
            { 
              title: 'hello 4',
              imgUrl: 'https://picsum.photos/200/300/?random',
              content: 'Lorem ipsum dummy content blah blah hello guys' 
            },
          ]
        },
        myBusiness: {
          listTitle: 'My Business',
          tag: 'my-business',
          data: [
            { 
              title: 'hello',
              imgUrl: 'https://picsum.photos/200/300/?random',
              content: 'Lorem ipsum dummy content blah blah hello guys' 
            },
            { 
              title: 'hello 2',
              imgUrl: 'https://picsum.photos/200/300/?random',
              content: 'Lorem ipsum dummy content blah blah hello guys' 
            },
            { 
              title: 'hello 3',
              imgUrl: 'https://picsum.photos/200/300/?random',
              content: 'Lorem ipsum dummy content blah blah hello guys' 
            },
            { 
              title: 'hello 4',
              imgUrl: 'https://picsum.photos/200/300/?random',
              content: 'Lorem ipsum dummy content blah blah hello guys' 
            },
          ]
        }
      }
    }
  },
  components: {
    Navigation,
    HeaderSlider,
    AppArticlePreviewList
  }
};
</script>
