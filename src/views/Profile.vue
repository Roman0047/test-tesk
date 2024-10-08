<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>
          <div class="title-wrapper">
            <ion-icon aria-hidden="true" :icon="logoIonic" />
            <div class="title">Profile</div>
          </div>
        </ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <div class="content">
        <div class="content-inner">
          <ion-icon aria-hidden="true" :icon="person" class="account-icon" />
          <div>
            <p><b>Phone:</b> 1231231231</p>
            <p><b>Email:</b> test@test.test</p>
            <p><b>Job title:</b> Test Job</p>
            <p><b>Company:</b> Test Company</p>
          </div>
        </div>
        <div class="social-buttons">
          <ion-button fill="clear">
            <ion-icon aria-hidden="true" :icon="logoFacebook" />
          </ion-button>
          <ion-button fill="clear">
            <ion-icon aria-hidden="true" :icon="logoGoogle" />
          </ion-button>
          <ion-button fill="clear">
            <ion-icon aria-hidden="true" :icon="logoTwitter" />
          </ion-button>
          <ion-button fill="clear">
            <ion-icon aria-hidden="true" :icon="logoLinkedin" />
          </ion-button>
        </div>
        <img class="qr-code" src="https://images.squarespace-cdn.com/content/v1/5d3f241fa4e0350001fa20d5/1636491460338-AIZAXV2978MGIDQE0GT7/qr-code.png" alt="">
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import {IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonIcon, IonButton} from '@ionic/vue';
import {logoFacebook, logoGoogle, logoIonic, logoLinkedin, logoTwitter, person} from 'ionicons/icons';
</script>

<style scoped>
.title {
  margin-left: 20px;
}

.title-wrapper {
  display: flex;
}

.account-icon {
  font-size: 100px;
  margin-right: 24px;
}

.content {
  height: 100%;
  display: flex;
  flex-direction: column;
  padding: 24px 24px;
}

.content-inner {
  display: flex;
  align-items: center;
}

.qr-code {
  width: 200px;
  margin: 40px auto;
  flex: 1;
  object-fit: contain;
}

.social-buttons {
  display: flex;
  justify-content: space-between;
  margin-top: 10px;
}
</style>
