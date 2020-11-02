<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Default</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Loading...</ion-title>
        </ion-toolbar>
      </ion-header>
    </ion-content>
  </ion-page>
</template>

<script>
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonContent,
} from '@ionic/vue'
import { useRouter } from 'vue-router'

export default {
  name: 'Tab1',
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage },
  mounted() {
    const router = useRouter()
    setTimeout(() => {
      router.replace('/tabs/tab1')
    }, 2000)
  },
}
</script>
