<template>
  <ion-page>

    <ion-header>
      <ion-toolbar>
        <ion-title>Postagram</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">

      <ion-fab vertical="top" horizontal="end" slot="fixed">
        <ion-fab-button tab="tab1" href="/tabs/tab1" color="dark">

          <ion-icon :icon="add"></ion-icon>
        </ion-fab-button>
      </ion-fab>

      <ion-card v-for="post in posts" v-bind:key="post.id">
        <ion-card-header>
          <ion-card-title>{{post.title}}</ion-card-title>
        </ion-card-header>

        <ion-card-content>
          {{post.content}}
        </ion-card-content>
      </ion-card>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonCard, IonIcon } from '@ionic/vue';
import {add} from 'ionicons/icons';


export default  {
  name: 'Tab2',
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonCard, IonIcon },

  data() {
    return {
      posts: [
        { id: 1, title: 'Mon initiation avec Vue', content: 'Vous voyez au-dessus que nous pouvons utilise utile qua exactement le contenu dont vous êtes en train' },
        { id: 2, title: 'Blogger avec Vue' , content: 'Vous voyez au-dessus que nous pouvons utilise utile qua exactement le contenu dont vous êtes en train' },
        { id: 3, title: 'Pourquoi Vue est tellement cool' , content: 'Vous voyez au-dessus que nous pouvons utilise utile qua exactement le contenu dont vous êtes en train' },
        { id: 1, title: 'Mon initiation avec Vue', content: 'Vous voyez au-dessus que nous pouvons utilise utile qua exactement le contenu dont vous êtes en train' },
        { id: 2, title: 'Blogger avec Vue' , content: 'Vous voyez au-dessus que nous pouvons utilise utile qua exactement le contenu dont vous êtes en train' },
        { id: 3, title: 'Pourquoi Vue est tellement cool' , content: 'Vous voyez au-dessus que nous pouvons utilise utile qua exactement le contenu dont vous êtes en train' }
      ]
    }
  },

  setup(){
    return{
      add
    }
  }



}


</script>
