<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Blank</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Carrito de Compra</ion-title>
        </ion-toolbar>
      </ion-header>

      <div id="container">
        <strong>Bienvenido al carrito de compra.</strong>
        <p>Por favor, inicia sesión para continuar.</p>
        <ButtonComponent href="/login" id="login" value="Iniciar sesion" expand="full" color="warning" />
        <ButtonComponent id="bypass_login" value="Entrar directamente" expand="full" color="danger" @click="loginwithnodata" />
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import ButtonComponent from '../components/ButtonComponent.vue';
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';


const user = ref('');
const password = ref('');

const loginwithnodata = () => {
  const username = user.value;
  const pass = password.value;

  if (username === '' && pass === '') {
    window.location.href = "/dashboard";
  } else {
    console.log('Credenciales inválidas');
  }
}
</script>

<style scoped>
#container {
  text-align: center;

  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;

  color: #8c8c8c;

  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>
