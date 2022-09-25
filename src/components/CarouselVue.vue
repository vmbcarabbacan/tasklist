<template>
    <v-carousel 
        :show-arrows="false" 
        hide-delimiters 
        cycle
        :height="$vuetify.display.lgAndUp ? 800 : 170"
    >
        <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
            cover
        />
  </v-carousel>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    setup() {
        const items = ref([
            {
                src: '	https://sikwin-test.netlify.app/assets/swiper3.c53a0aaf.png',
            },
            {
                src: '	https://sikwin-test.netlify.app/assets/swiper3.c53a0aaf.png',
            },
        ])

        return {
            items
        }
    }
})
</script>
