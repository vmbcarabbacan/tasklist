<template>
    <div>
        <carousel-vue />
        <v-container class="mt-1">
            <v-row>
                <v-col
                    cols="12"
                >
                    <hot-games />
                </v-col>
                <v-col
                    cols="12"
                >
                    <user-name />
                </v-col>
                <v-col
                    cols="12"
                >
                    <sport-games />
                </v-col>
                <v-col
                    cols="12"
                >
                    <bottom-navigation />
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>
<script>
import { defineComponent } from 'vue'
import CarouselVue from './CarouselVue.vue';
import HotGames from './HotGames.vue';
import UserName from './UserName.vue';
import SportGames from './SportGames.vue';
import bottomNavigation from './bottomNavigation.vue';

export default defineComponent({
    components: {
        CarouselVue,
        HotGames,
        UserName,
        SportGames,
        bottomNavigation,
    },

    setup() {
        
    },
})
</script>
