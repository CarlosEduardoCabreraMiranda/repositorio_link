<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Carrito de compra</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content>
      <div id="login-container">
        <div id="login-form">
          <BasicUserInput />
          <InputComponent id="metodo_pago" name="metodo_pago" label="Metodo de pago:" color="success" />
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
  import CrudButtonComponent from '../components/CrudButtonComponent.vue';
  import BasicUserInput from '@/components/BasicUserInput.vue';
  import InputComponent from '../components/InputComponent.vue';
import ButtonComponent from '@/components/ButtonComponent.vue';
  </script>
  
  <style scoped src="../theme/container.css"></style>

