<template>
    <q-card style="margin-bottom:16px; background: #fff">
        <q-item class="no-margin no-padding" style="padding-top: 15px; overflow: hidden;" v-if="contenu === 'news-high'">
            <q-card-media style="padding: 0">
                <div class="img-header">
                    <img src="/statics/9a920f75-c1cf-4a92-8236-c74a7f928599.jpg" style="width: 100%;">
                </div>
                <q-card-title slot="overlay">
                    <q-item-side avatar="/statics/boy2.svg"/>
                    <q-item-main>
                        <div class="col-6 column" style="font-size: 30px; font-weight: bold;">
                            <span slot="subtitle" style="font-size: 20px;">[{{author}}]</span>
                            {{title}}
                        </div>
                    </q-item-main>
                </q-card-title>
            </q-card-media>
        </q-item>
        <q-item style="padding-top: 15px;" v-else>
            <q-item-side avatar="/statics/boy2.svg"/>
            <q-item-main>
                <div class="col-6 column" style="font-size: 25px; font-weight: bold;">{{title}}
                    <span slot="subtitle" style="font-size: 20px;">[{{author}}]</span>
                </div>
            </q-item-main>
        </q-item>
        <q-item>
            <p class="text-justify no-margin">{{text}}</p>
        </q-item>
        <q-card-actions>
            <q-item class="date-news">{{date}}</q-item>
            <q-btn flat>
                <q-icon name="comment" />
            </q-btn>
            <q-btn flat>
                <q-icon name="share" />
            </q-btn>
        </q-card-actions>
        <!-- Show Video -->
        <q-card-media v-if="contenu === 'video'">
            <q-video src="https://www.youtube.com/embed/LYU-8IFcDPw" style=" height: 310px" />
        </q-card-media>
        <!-- Show Gallery -->
        <q-card-media v-if="contenu === 'gallery'">
            <div class="container">
                <div class="left">
                    <div class="row no-margin" style="padding: 0 5px 5px 0 ">
                        <img style="height: 105px;" src="https://picsum.photos/200">
                    </div>
                    <div class="row no-margin">
                        <img style="height: 105px;" src="https://picsum.photos/200">
                    </div>
                </div>
                <div class="no-margin no-padding right" style="width: auto; height:215px; overflow: hidden">
                    <img src="https://picsum.photos/1200">
                </div>
            </div>
        </q-card-media>

        <!-- border bottom -->
        <div class="row justify-around no-margin" style="background: #E8A021; height: 6px">
        </div>
    </q-card>
</template>
<style>
    .container {
        width:100%;
        display: flex;
    }
    .left {
        float: left;
    }
    .right {
        width:auto;
        float:right;
    }
    .q-item-avatar, .q-item-avatar img{
        width: 55px;
        height:55px;
        border-radius: 0;
        padding-top:6px;
    }
    .date-news {
        padding: 0px 8px;
        font-style: italic;
        font-size: 13px;
        min-height: 30px;
        color: #999;
    }
    .q-card-media-overlay{
        /*background: none;*/
        background: -moz-linear-gradient(bottom, rgba(0,0,0,1) 0%, rgba(0,0,0,0) 100%); /* FF3.6-15 */
        background: -webkit-linear-gradient(bottom, rgba(0,0,0,1) 0%,rgba(0,0,0,0) 100%); /* Chrome10-25,Safari5.1-6 */
        background: linear-gradient(to top, rgba(0,0,0,1) 0%,rgba(0,0,0,0) 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
    }
    .q-card-media .q-item-side{
        float: left;
        padding-right: 10px;
    }
    .q-card-media .q-item-main, .q-card-media .q-item-main span {
        color: #FFF;
    }
    .q-item-main span{
        color: #E8A021;
    }
    .q-card-media .q-item-side .q-item-avatar, .q-card-media .q-item-side .q-item-avatar img{
        padding:0;
        margin-top:4px;
    }
    .q-card-container{
        padding: 16px 16px 6px 16px;
    }
    .q-card-media .img-header{
        max-height:180px;
        overflow: hidden;

    }
</style>
<script>
  import {
    QBtn,
    QIcon,
    QItem,
    QItemSide,
    QCard,
    QVideo,
    QCardTitle,
    QCardMedia,
    QCardActions,
    QItemMain
  } from 'quasar'
  export default {
    props: ['id', 'contenu', 'title', 'author', 'text', 'date'],
    components: {
      QVideo,
      QCard,
      QCardTitle,
      QCardMedia,
      QCardActions,
      QBtn,
      QIcon,
      QItem,
      QItemSide,
      QItemMain
    }
  }
</script>