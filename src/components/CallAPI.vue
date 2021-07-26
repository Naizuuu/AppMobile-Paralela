<template>
    <!-- List of Text Items -->
    <ion-list>
        <ion-item>
            <ion-thumbnail slot="start">
                <img src="../assets/img/earthquake.png">
                <div class="centrado">
                    <strong>4.2 Mw</strong>
                </div>
            </ion-thumbnail>
            <ion-label>
                <h3>9 km al O de El Tabo</h3>
                <p>2021/07/26 16:58:06</p>
            </ion-label>
        </ion-item>
        <!-- <ion-item>
            <ion-thumbnail slot="start">
                <img src="../assets/img/earthquake.png">
                <div class="centrado">
                    <strong>4.2</strong>
                    Mw
                </div>
            </ion-thumbnail>
            <ion-label>
                <h3>9 km al O de El Tabo</h3>
                <p>2021/07/26 16:58:06</p>
            </ion-label>
        </ion-item> -->
    </ion-list>
</template>

<script>
import { 
    IonItem, 
    IonList, 
    IonLabel,
    IonThumbnail
} from '@ionic/vue';

import { defineComponent } from 'vue';

export default defineComponent({
    components: {
        IonItem,
        IonList,
        IonLabel,
        IonThumbnail
    }
});
</script>

<style scoped>
    ion-thumbnail {
        position: relative;
        display: inline-block;
        text-align: center;
    }

    .centrado {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: black;
    }
</style>