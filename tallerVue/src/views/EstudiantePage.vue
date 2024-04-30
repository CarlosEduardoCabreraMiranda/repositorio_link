<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Prodcuto</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content>
      <div id="login-container">
        <div id="login-form">
          <BasicUserInput />
          <InputComponent type="number" id="edad" name="edad" label="Edad: " />
        </div>

        <div>
          <!--Traer el componente de los botones de la crud  -->
          <CrudButtonComponent />

          <ButtonComponent href="/dashboard" value="Ir a dashboard" id="backBtn" />
        </div>
      </div>
    </ion-content>
  </ion-page>
</template>
  
  <script setup lang="ts">
  import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
  import ButtonComponent from '@/components/ButtonComponent.vue';
  import InputComponent from '@/components/InputComponent.vue';
  import CrudButtonComponent from '@/components/CrudButtonComponent.vue';
import BasicUserInput from '@/components/BasicUserInput.vue';
  </script>
  
  <style scoped src="../theme/container.css"></style>

