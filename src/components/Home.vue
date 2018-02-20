<template>
 <q-layout
    ref="layout"
    view="lHh Lpr fff"
    :left-class="{'bg-grey-2': true}"
  >
    <q-toolbar slot="header" class="glossy">
      <q-btn>
        <q-icon name="menu" />
      </q-btn>

      <q-toolbar-title>
        Quasar App
        <div slot="subtitle">Running on Quasar v{{$q.version}}</div>
      </q-toolbar-title>
    </q-toolbar>
<div class="main" style="position: relative; width:540px; margin-left:50%; left: -270px;">

    <!-- implement a card list -->
    <card-news
            v-for="item in cardList"
            v-bind:key="id"
            v-bind="item"/>

    <!--<q-card>
        <q-item>
            <q-item-side avatar="/statics/boy.svg" />
            <q-item-main>
                <q-item-tile label>Title</q-item-tile>
                <q-item-tile sublabel>Subhead</q-item-tile>
            </q-item-main>
        </q-item>
        <q-item class="row justify-around items-center md-gutter">
            <div >
                <p class="col-10">{{lorem}}</p>
            </div>
        </q-item>
        <q-card-actions>
            <q-btn flat>
                <q-icon name="comment" />
            </q-btn>
            <q-btn flat>
                <q-icon name="share" />
            </q-btn>
        </q-card-actions>
    </q-card>

    <q-card>
        <q-card-title>
            <div class="row items-start items-center">
                <div class="col-1"><q-item-side avatar="/statics/boy.svg" /> </div>
                <div class="col-6 column" > Title <span slot="subtitle">Subtitle</span></div>
            </div>
        </q-card-title>
        <q-card-main>
            <q-item class="row justify-around items-center md-gutter">
                <div >
                    <p class="col-10">{{lorem}}</p>
                </div>
            </q-item>
        </q-card-main>
        <q-card-media class=" row justify-around">
            <div class="row">
                <div>
                    <div class="row">
                        <img style="height: 150px;" src="https://picsum.photos/200">
                    </div>
                    <div class="row">
                        <img style="height: 150px;" src="https://picsum.photos/200">
                    </div>
                </div>

                <div>
                    <div>
                        <img style="height: 300px;" src="https://picsum.photos/1200">
                    </div>
                </div>
            </div>
        </q-card-media>
        <q-card-actions>
            <q-btn flat>
                <q-icon name="comment" />
            </q-btn>
            <q-btn flat>
                <q-icon name="share" />
            </q-btn>
        </q-card-actions>
    </q-card>

    <q-card>

        <q-card-title>
            <div class="row items-start items-center">
                <div class="col-1"><q-item-side avatar="/statics/boy.svg" /> </div>
                <div class="col-6 column" > Title <span slot="subtitle">Subtitle</span></div>
            </div>
        </q-card-title>

        <q-card-main class="row">
            <div class="justify-around"> petite vidéo de moi entrain de jouer sous ma douche tranquillement .... et un peut plus de texte pour l'exemple </div>
        </q-card-main>

        <q-card-media>
            <div class="row justify-around md-gutter">
                <q-video class="col-10 " style=" height: 450px" src="https://www.youtube.com/embed/k3_tw44QsZQ?rel=0"/>
            </div>
        </q-card-media>

        <q-card-actions>
            <q-btn flat>
                <q-icon name="comment" />
            </q-btn>
            <q-btn flat>
                <q-icon name="share" />
            </q-btn>
        </q-card-actions>



    </q-card>
    <q-card>
        <q-card-title>
            <div class="row items-start items-center">
                <div class="col-1"><q-item-side avatar="/statics/boy.svg" /> </div>
                <div class="col-6 column" > Title <span slot="subtitle">Subtitle</span></div>
            </div>
        </q-card-title>

        <q-card-main>
            <q-item class="row justify-around items-center md-gutter">
                <div >
                    <p class="col-10">{{lorem}}</p>
                </div>
            </q-item>
        </q-card-main>

        <q-card-actions>
            <q-btn flat>
                <q-icon name="comment" />
            </q-btn>
            <q-btn flat>
                <q-icon name="share" />
            </q-btn>
        </q-card-actions>
    </q-card>-->
</div>
  </q-layout>
</template>
<style>
    body{
        background: #f4f4f4;
    }
</style>
<script>
import {
  QLayout,
  QToolbar,
  QToolbarTitle,
  QBtn,
  QIcon,
  QList,
  QListHeader,
  QItem,
  QItemSide,
  QCard,
  QVideo,
  QCardTitle,
  QCardMedia,
  QCardActions,
  QCardSeparator,
  QCardMain,
  QItemMain
} from 'quasar'
import CardNews from './CardNews.vue'

export default {
  name: 'index',
  components: {
    QLayout,
    QVideo,
    QCard,
    QCardTitle,
    QCardMedia,
    QCardActions,
    QCardSeparator,
    QCardMain,
    QToolbar,
    QToolbarTitle,
    QBtn,
    QIcon,
    QList,
    QListHeader,
    QItem,
    QItemSide,
    QItemMain,
    CardNews
  },
  data () {
    return {
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      cardList: [
        {id: 0, contenu: 'video', title: 'Faint - Official video', author: 'Linkin\' Park', date: '04 fév. 10h12', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'},
        {id: 1, contenu: 'gallery', title: 'Test2', author: 'Author', date: '04 fév. 10h12', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'},
        {id: 2, contenu: 'news-high', title: 'Test3', author: 'Author', date: '04 fév. 10h12', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'},
        {id: 3, title: 'Test4', author: 'Author', date: '04 fév. 10h12', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'},
        {id: 3, contenu: 'video', title: 'Test5', author: 'Author', date: '04 fév. 10h12', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'}
      ]
    }
  }
}
</script>
