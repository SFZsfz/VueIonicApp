<template>
  <ion-page>

    <ion-header>
      <ion-toolbar>
        <ion-title>Ajouter</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">

      <form v-on:submit.prevent="onSubmit()" method="POST">
        <ion-item style="margin-top: 5px">
          <ion-label>Titre du Post</ion-label>
          <ion-input v-model="title" required></ion-input>

        </ion-item>

        <ion-item style="margin-top: 5px">
          <ion-label>Contenu du post</ion-label>
          <ion-input v-model="content" required></ion-input>
        </ion-item>

        <ion-button color="light" type="submit" >Ajouter</ion-button>

      </form>

    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonInput } from '@ionic/vue';

export default {
  name: 'Tab1',
  components: {IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonInput},


  data() {
    return {};
  },
  methods: {
    title: '',
    content: '',
    onSubmit() {
      const data = {
        title: this.title,
        content: this.content
      };
      console.log(data)



    }
  }
}

</script>
