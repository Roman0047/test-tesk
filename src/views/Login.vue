<template>
  <ion-content>
    <div class="content">
      <h2>Login to your account</h2>
      <div class="input-wrapper">
        <ion-input
            type="email"
            fill="solid"
            label="Email"
            label-placement="floating"
            @ionInput="user.email = $event.target.value"
        ></ion-input>
      </div>

      <div class="input-wrapper">
        <ion-input
            type="password"
            fill="solid"
            label="Password"
            label-placement="floating"
            @ionInput="user.password = $event.target.value"
        ></ion-input>
      </div>

      <ion-button expand="full" :disabled="!user.email || !user.password" href="/profile">
        Sign In
      </ion-button>
    </div>
  </ion-content>
</template>

<script setup lang="ts">
import {IonContent, IonInput, IonButton} from '@ionic/vue';
import { ref } from 'vue';

const user = ref<any>({
  email: '',
  password: '',
});
</script>

<style scoped>
h2 {
  margin-bottom: 20px
}

.content {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0 24px;
}

.banner {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0 24px;
  text-align: center;
}

.input-wrapper {
  margin-bottom: 24px;
}
</style>