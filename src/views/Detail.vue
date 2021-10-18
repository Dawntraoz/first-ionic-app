<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Detail</ion-title>
        <ion-buttons slot="start">
          <ion-back-button default-href="/"></ion-back-button>
        </ion-buttons>
      </ion-toolbar>
    </ion-header>
    
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Detail</ion-title>
        </ion-toolbar>
      </ion-header>

      <p>The dynamic ID is {{ id }}</p>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonButtons, IonBackButton } from '@ionic/vue';
import { useRoute } from 'vue-router';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Detail',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonButtons, IonBackButton,
  },
  setup() {
    const route = useRoute()
    const id = route.params.id
    return { id }
  }
});
</script>

<style scoped>
</style>