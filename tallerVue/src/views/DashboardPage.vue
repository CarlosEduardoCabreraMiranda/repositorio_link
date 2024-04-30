<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Dashboard</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content>
      <br>
      <div id="container">
        <strong>
          <ButtonComponent href="/cliente" value="Ir a Cliente" id="clientesBtn" />
        </strong>
        <br>

        <strong>
          <ButtonComponent href="/estudiante" value="Ir a Estudiante" id="estudiantesBtn" />
        </strong>

        <strong>
          <ButtonComponent href="/empleado" value="Ir a Empleado" id="empleadoBtn" />
        </strong>
      </div>

    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import ButtonComponent from '../components/ButtonComponent.vue';
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
</script>

<style scoped></style>
