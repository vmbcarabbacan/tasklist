<template>
    <v-card class="mt-12" >
        <v-card-title>
            <p class="text-md-h3 text-yellow-lighten-2">Hot Game</p>
        </v-card-title>
        <v-card-item>
            <v-row>
                <v-col
                    :cols="$vuetify.display.lgAndUp ? 2 : 3"
                    v-for="(item, i) in bonanzas"
                    :key="i"
                    >
                    <v-card
                    >
                        <v-img :src="item.src" :lazy-src="item.src"></v-img>
                    </v-card>
                </v-col>
            </v-row>
        </v-card-item>
    </v-card>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    setup() {
        const bonanzas = ref([
            {
                src: 'https://sikwin-test.netlify.app/assets/imageList.b86c905a.jpg'
            },
            {
                src: 'https://sikwin-test.netlify.app/assets/imageList.b86c905a.jpg'
            },
            {
                src: 'https://sikwin-test.netlify.app/assets/imageList.b86c905a.jpg'
            },
            {
                src: 'https://sikwin-test.netlify.app/assets/imageList.b86c905a.jpg'
            },
        ]);

        return {
            bonanzas
        }
    },
})
</script>
