<template>
  <ion-page>
    <ion-content :fullscreen="true">

      <ion-list v-for="(value ) in infos" v-bind:key="value">
        {{value.bpi}}
      </ion-list>

      <br>

      {{this.infos.bpi}}


    </ion-content>
    <ion-header>
      <ion-toolbar>
        <ion-title>Stats</ion-title>
      </ion-toolbar>
    </ion-header>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonList } from '@ionic/vue';
import axios from "axios";

export default  {
  name: 'Tab3',
  components: {IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonList},
  infos: '',


  data () {
    return {
      infos: ''
    }
  },
  async mounted() {
     {
      axios.get('https://api.coindesk.com/v1/bpi/currentprice.json').then((e: string) => {
        this.infos = e
      })
    }
  },




}
</script>
