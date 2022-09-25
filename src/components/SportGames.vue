<template>
    <v-card>
      <v-row>
        <v-col cols="3" md="2" sm="3">
            <v-tabs
                v-model="tab"
                background-color="primary"
                direction="vertical"
                height="350"
            >
                <v-tab value="live" class="justify-center">
                    <v-avatar
                        :size="$vuetify.display.mdAndUp ? 80 : 50"
                        rounded="0"
                    >
                        <v-img 
                            src="https://sikwin-test.netlify.app/assets/ho_li2@3x.1f8b69c5.png"
                            lazy-src="https://sikwin-test.netlify.app/assets/ho_li2@3x.1f8b69c5.png"
                            />
                    </v-avatar>
                </v-tab>
                <v-tab value="sports" class="justify-center">
                    <v-avatar
                        :size="$vuetify.display.mdAndUp ? 80 : 50"
                        rounded="0"
                    >
                        <v-img 
                            src="https://sikwin-test.netlify.app/assets/ho_sp2@3x.2d641946.png"
                            lazy-src="https://sikwin-test.netlify.app/assets/ho_sp2@3x.2d641946.png"
                            />
                    </v-avatar>
                </v-tab>
                <v-tab value="lottery" class="justify-center">
                    <v-avatar
                        :size="$vuetify.display.mdAndUp ? 80 : 50"
                        rounded="0"
                    >
                        <v-img 
                            src="https://sikwin-test.netlify.app/assets/ho_lo2@3x.92942dc8.png"
                            lazy-src="https://sikwin-test.netlify.app/assets/ho_lo2@3x.92942dc8.png"
                            />
                    </v-avatar>
                </v-tab>
                <v-tab value="poker" class="justify-center">
                    <v-avatar
                        :size="$vuetify.display.mdAndUp ? 80 : 50"
                        rounded="0"
                    >
                        <v-img 
                            src="https://sikwin-test.netlify.app/assets/ho_po2@3x.00c06826.png"
                            lazy-src="https://sikwin-test.netlify.app/assets/ho_po2@3x.00c06826.png"
                            />
                    </v-avatar>
                </v-tab>
                <v-tab value="game" class="justify-center">
                    <v-avatar
                        :size="$vuetify.display.mdAndUp ? 80 : 50"
                        rounded="0"
                    >
                        <v-img 
                            src="https://sikwin-test.netlify.app/assets/ho_ga2@3x.0a2e93ac.png"
                            lazy-src="https://sikwin-test.netlify.app/assets/ho_ga2@3x.0a2e93ac.png"
                            />
                    </v-avatar>
                </v-tab>
            </v-tabs>
        </v-col>
        <v-col cols="6">
            <v-card-text>
                <v-window v-model="tab">
                <v-window-item value="live">
                    <v-row>
                        <v-col
                            cols="12"
                            v-for="(item, i) in lives"
                            :key="i"
                            >
                            <v-card
                            >
                                <v-img :src="item.src" :lazy-src="item.src"></v-img>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-window-item>
        
                <v-window-item value="sports">
                    <v-row>
                        <v-col
                            cols="12"
                            v-for="(item, i) in sports"
                            :key="i"
                            >
                            <v-card
                            >
                                <v-img :src="item.src" :lazy-src="item.src"></v-img>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-window-item>
        
                <v-window-item value="lottery">
                    <v-row>
                        <v-col
                            cols="12"
                            v-for="(item, i) in lives"
                            :key="i"
                            >
                            <v-card
                            >
                                <v-img :src="item.src" :lazy-src="item.src"></v-img>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-window-item>
                <v-window-item value="poker">
                    <v-row>
                        <v-col
                            cols="12"
                            v-for="(item, i) in sports"
                            :key="i"
                            >
                            <v-card
                            >
                                <v-img :src="item.src" :lazy-src="item.src"></v-img>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-window-item>
                <v-window-item value="game">
                    <v-row>
                        <v-col
                            cols="12"
                            v-for="(item, i) in games"
                            :key="i"
                            >
                            <v-card
                            >
                                <v-img :src="item.src" :lazy-src="item.src"></v-img>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-window-item>
                </v-window>
            </v-card-text>
        </v-col>
      </v-row>
    </v-card>
  </template>

  <script>
  import { defineComponent, ref } from 'vue'
  
  export default defineComponent({
    setup() {
        const tab = ref();
        const lives = ref([
            {
                src: 'https://sikwin-test.netlify.app/assets/game-image-2.000b53bd.png'
            },
            {
                src: 'https://sikwin-test.netlify.app/assets/game-image-2.000b53bd.png'
            },
            {
                src: 'https://sikwin-test.netlify.app/assets/game-image.dcbb90ad.png'
            },
            {
                src: 'https://sikwin-test.netlify.app/assets/game-image.dcbb90ad.png'
            },
        ]);
        const sports = ref([
            {
                src: 'https://sikwin-test.netlify.app/assets/game-image.dcbb90ad.png'
            },
            {
                src: 'https://sikwin-test.netlify.app/assets/game-image-2.000b53bd.png'
            },
            {
                src: 'https://sikwin-test.netlify.app/assets/game-image.dcbb90ad.png'
            },
        ]);
        const games = ref([
            {
                src: 'https://sikwin-test.netlify.app/assets/game-image.dcbb90ad.png'
            },
            {
                src: 'https://sikwin-test.netlify.app/assets/game-image.dcbb90ad.png'
            },
        ]);

        return {
            tab,
            lives,
            sports,
            games
        }
    },
  })
  </script>
  
  <style>
    .v-tab.v-tab.v-tab {
        height: 100px;
    }
    .v-btn.v-btn--density-default {
        height: 100px;
    }

    @media only screen and (max-width: 600px) {
        .v-tab.v-tab.v-tab {
            height: 70px;
        }
        .v-btn.v-btn--density-default {
            height: 70px;
        }
    }
  </style>