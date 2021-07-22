<template>
    <ion-page>

        <ion-header>
            <ion-toolbar>
                <ion-title class="ion-margin-top">Integrantes</ion-title>
            </ion-toolbar>
        </ion-header>

        <ion-content :fullscreen="true">
            <ion-header collapse="condense">
                <ion-toolbar>
                    <ion-title size="large">Tab 2</ion-title>
                </ion-toolbar>
            </ion-header>
            <ExploreContainer name="Integrantes"/>
        </ion-content>

    </ion-page>
</template>

<script lang="ts">
    import { 
        IonPage, 
        IonHeader, 
        IonToolbar, 
        IonTitle, 
        IonContent 
    } from '@ionic/vue';

import ExploreContainer from '@/components/ExploreContainer.vue';

    export default  {
        name: 'Tab1',
        components: 
        { 
            ExploreContainer,
            IonHeader,
            IonToolbar,
            IonTitle,
            IonContent,
            IonPage
        }
    }
</script>