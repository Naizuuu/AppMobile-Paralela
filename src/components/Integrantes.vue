<template>
    <ion-card>
        <img src="../assets/img/AJ.jpg">
        <ion-card-header>
        <ion-card-subtitle>Desarrollador</ion-card-subtitle>
        <ion-card-title>Axel Jeréz</ion-card-title>
        </ion-card-header>

        <ion-card-content>
        Estudiante ingresado el año 2016 a la carrera Ingeniería Civil en Computación mención en Informática. 
        Actualmente cursando la asignatura de Computación Paralela y Distribuida.
        </ion-card-content>
    </ion-card>

    <ion-card>
        <img src="../assets/img/SM.jpg">
        <ion-card-header>
        <ion-card-subtitle>Desarrollador</ion-card-subtitle>
        <ion-card-title>Sebastián Muñoz</ion-card-title>
        </ion-card-header>

        <ion-card-content>
        Estudiante ingresado el año 2016 a la carrera Ingeniería Civil en Computación mención en Informática. 
        Actualmente cursando la asignatura de Computación Paralela y Distribuida.
        </ion-card-content>
    </ion-card>
</template>

<script lang="ts">
import { IonCard, IonCardContent, IonCardHeader, IonCardSubtitle, IonCardTitle } from '@ionic/vue';

import { defineComponent } from 'vue';

export default defineComponent({
    components: { 
        IonCard, 
        IonCardContent, 
        IonCardHeader, 
        IonCardSubtitle, 
        IonCardTitle
    }
});
</script>

<style scoped>
    img {
        object-fit: cover;
        object-position: 100% 0;
        width: auto;
        height: 100vw;
        min-width: 100%;
    }
</style>