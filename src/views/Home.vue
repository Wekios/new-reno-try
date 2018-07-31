<template>
  <div class="home">
    <!-- <test-component :data="homepage[0]"/>
    <app-article-preview-list class="article-preview-list" :data="homepage[1]"/> -->
    <component v-for="(component,index) in homepage" :is="component.type" :data="component" :key="index">
    </component>
  </div>
</template>

<script>
import Navigation from "@/components/Navigation/Navigation.vue";
import TestComponent from "@/components/Test/TestComponent";
import AppArticlePreviewList from "@/components/Articles/ArticlePreviewList";

export default {
  name: "home",
  data() {
    return {
      homepage: [
        {
          type: "test-component",
          class: "Layout2",
          data: {
            custom_item_name: "",
            item_id: "62",
            item_name: "HP Slider"
          },
          element_item: {
            id: 62,
            title: "HP Slider"
          }
        },
        {
          type: "app-article-preview-list",
          class: "layout1",
          data: {
            custom_item_name: "NEWS of the WEEK",
            item_id: "1",
            item_name: "HP Latest All"
          },
          element_item: {
            name: "HP Latest All",
            list_items: [
              {
                id: 1,
                title: "MY VAN & TRAFFIC REGULATION",
                category: [
                  {
                    id: 16,
                    name: "Faq"
                  }
                ],
                featured_image: [
                  {
                    data: {
                      file: {
                        url:
                          "http://harmony-assets-live.s3.amazonaws.com/diwanee_corp_images/69/fe/69fe15cece1f526f425b6e01a6f5a7ff.jpg",
                        hash: "69fe15cece1f526f425b6e01a6f5a7ff"
                      },
                      seoname:
                        "Everything you have to know to master roads and regulation with your van",
                      seoalt:
                        "Everything you have to know to master roads and regulation with your van",
                      caption:
                        "Everything you have to know to master roads and regulation with your van",
                      copyright: ""
                    }
                  }
                ],
                images: [],
                additional_fields: {
                  intro:
                    "Check our FAQs to get an overview of traffic regulation."
                }
              },
              {
                id: 2,
                title: "MY CAR VS MY VAN",
                category: [
                  {
                    id: 16,
                    name: "Faq"
                  }
                ],
                featured_image: [
                  {
                    data: {
                      file: {
                        url:
                          "http://harmony-assets-live.s3.amazonaws.com/diwanee_corp_images/97/98/9798c8b9f341b7bdd5c5096d7a20d028.jpg",
                        hash: "9798c8b9f341b7bdd5c5096d7a20d028"
                      },
                      seoname: "My car Vs My van",
                      seoalt: "My car Vs My van",
                      caption: "My car Vs My van",
                      copyright: ""
                    }
                  }
                ],
                images: [],
                additional_fields: {
                  intro:
                    "Check our FAQs to know everything about the specificities of your van."
                }
              },
              {
                id: 3,
                title: "SECURITY IN MY VAN",
                category: [
                  {
                    id: 16,
                    name: "Faq"
                  }
                ],
                featured_image: [
                  {
                    data: {
                      file: {
                        url:
                          "http://harmony-assets-live.s3.amazonaws.com/diwanee_corp_images/a3/0b/a30b8a0d0a9f04e1e17013cbc061e029.jpg",
                        hash: "a30b8a0d0a9f04e1e17013cbc061e029"
                      },
                      seoname: "Security in my van",
                      seoalt: "Security in my van",
                      caption: "Security in my van",
                      copyright: ""
                    }
                  }
                ],
                images: [],
                additional_fields: {
                  intro:
                    "Check our FAQs to know everything you need about security."
                }
              },
              {
                id: 4,
                title: "PARKING MY VAN",
                category: [
                  {
                    id: 16,
                    name: "Faq"
                  }
                ],
                featured_image: [
                  {
                    data: {
                      file: {
                        url:
                          "http://harmony-assets-live.s3.amazonaws.com/diwanee_corp_images/c0/f5/c0f56e17db5eba597963fd71425dba05.jpg",
                        hash: "c0f56e17db5eba597963fd71425dba05"
                      },
                      seoname: "Parking my van",
                      seoalt: "Parking my van",
                      caption: "Parking my van",
                      copyright: ""
                    }
                  }
                ],
                images: [],
                additional_fields: {
                  intro:
                    "Check our FAQs to know everything you need about parking your van."
                }
              }
            ]
          }
        }
      ]
    };
  },
  components: {
    Navigation,
    TestComponent,
    AppArticlePreviewList
  },
  mounted() {
    console.log(this.homepage[1].element_item.list_items);
  }
};
</script>

<style lang="scss" scoped>
.home {
  display: grid;
  width: 85%;
  margin: 0 auto;
}
</style>

