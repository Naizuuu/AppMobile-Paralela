<template>
    <!-- List of Text Items -->
    <ion-list>
        <ion-item>
            <ion-label>
                <p>Información de los últimos 15 sismos.</p>
            </ion-label>
        </ion-item>
        <ion-item-sliding v-for="dato in datos" :key="dato.id">
            <ion-item>
                <ion-thumbnail slot="start">
                    <img src="../assets/img/earthquake.png">
                    <div class="centrado">
                        <strong>{{dato.magnitud}}</strong>
                    </div>
                </ion-thumbnail>
                <ion-label>
                    <h3>{{dato.georef}}</h3>
                    <p>{{dato.fecha}}</p>
                </ion-label>
            </ion-item>
            <ion-item-options side="end">
                <ion-item-option @click="unread(item)">
                    <ion-icon slot="icon-only" :icon="informationCircle"></ion-icon>
                </ion-item-option>
            </ion-item-options>
        </ion-item-sliding>
    </ion-list>
</template>

<script>
import { 
    IonItem, 
    IonList, 
    IonLabel,
    IonThumbnail,
    IonItemSliding,
    IonItemOption, 
    IonItemOptions,
    IonIcon
} from '@ionic/vue';

import { informationCircle } from 'ionicons/icons';

import { defineComponent } from 'vue';
import axios from 'axios';

export default defineComponent({
    components: {
        IonItem,
        IonList,
        IonLabel,
        IonThumbnail,
        IonItemSliding,
        IonItemOption, 
        IonItemOptions,
        IonIcon
    },
    setup() {
            return {
                informationCircle
            }
    },
    mounted() {
        this.getDatos();
    },
    methods: {
        getDatos() {
            axios.get('http://127.0.0.1:8000/earthquakes', {
                headers: {
                    Authorization: 'Bearer ' + '1|JOLV9xU1YNyurXHxNR9zDapSdXl2hNpjfeOkCcHn',
                    'Content-Type' : 'application/json',
                    'Accept' : 'application/json'
                }
            })
                    .then(response => {
                        this.datos = response.data
                    })
                    .catch(e => console.log(e))
        }
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

    .centrado > strong {
        text-shadow: 2px 2px 0px rgba(0,0,0,0.6);
        color: white;
    }
</style>