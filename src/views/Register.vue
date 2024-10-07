<template>
  <ion-content>
    <div v-if="!isCompleted" class="content">
      <h2>Create your account</h2>
      <div class="input-wrapper">
        <ion-input
          type="number"
          fill="solid"
          label="Phone"
          label-placement="floating"
          @ionInput="user.phone = $event.target.value"
        ></ion-input>
      </div>

      <div class="input-wrapper">
        <ion-input
            fill="solid"
            label="Job title"
            label-placement="floating"
            @ionInput="user.job = $event.target.value"
        ></ion-input>
      </div>

      <div class="input-wrapper">
        <ion-input
            fill="solid"
            label="Company"
            label-placement="floating"
            @ionInput="user.company = $event.target.value"
        ></ion-input>
      </div>

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

      <div class="input-wrapper">
        <ion-input
          type="password"
          fill="solid"
          label="Repeat Password"
          label-placement="floating"
          @ionInput="user.repeatPassword = $event.target.value"
        ></ion-input>
      </div>

      <ion-button expand="full" :disabled="!user.phone || !user.email || !user.password || !user.repeatPassword || !user.job || !user.company" @click="isCompleted = true">
        Sign Up
      </ion-button>
    </div>
    <div v-else class="banner">
      <h1>Your account has been created successfully</h1>
      <ion-button expand="full" href="/login">
        Go to the login page
      </ion-button>
    </div>
  </ion-content>
</template>

<script setup>
import { ref } from 'vue';

const isCompleted = ref(false)
const user = ref({
  phone: '',
  email: '',
  password: '',
  repeatPassword: '',
  job: '',
  company: ''
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