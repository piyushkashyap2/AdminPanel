<template>
    <div>
        <h5 class="q-mx-sm">Dashboard</h5>
    </div>
    <q-page>
        <q-scroll-area class="full-width" style="height: 140px;">
            <div class="row no-wrap" style="height: 100px;">
                <q-card class="q-mx-sm" v-for="(head, index) in heads" :key="index"
                    style="width: 200px; height:120px; border-radius: 10px; background: radial-gradient(circle, #35a2ff 0%, #014a88 100%)">
                    <div class=" row ">
                        <div class=" col q-mx-sm q-my-md">
                            <div class="text-white text-bold" style="font-size: 12px; height:18px">
                                {{ head.content }}
                            </div>
                            <div class="text-white" style="font-size: 17px; height:40px">
                                3,930
                            </div>
                            <div class="text-white" style="font-size: 12px;">
                                Increased by 10%
                            </div>
                        </div>
                        <div class="q-my-md q-mx-sm">
                            <q-icon name="notepad" color="white"></q-icon>
                        </div>
                    </div>



                </q-card>
            </div>

        </q-scroll-area>
        <!-- <q-card>
            <div class="items-center no-wrap" style="height: 420px;">
                <q-card class="q-mx-sm bg-blue" style="border-radius: 10px; height: 400px">
                    <q-card-section class="flex">
                        <div class="bg-blue ">Graph</div>
                        <div class="bg-red">hii
                        </div>
                    </q-card-section>
                </q-card>
            </div>
        </q-card> -->
        <q-card>
            <div class="q-pa-md">
                <q-table :rows="rows" row-key="name" flat bordered />
            </div>
        </q-card>
        <q-card class="q-my-sm bg-blue-grey-2" style="width:500px; ">
            <div class="q-pa-md">
                <q-carousel animated v-model="slide" arrows navigation infinite>
                    <q-carousel-slide :name="1" img-src="https://cdn.quasar.dev/img/mountains.jpg" />
                    <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg" />
                    <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg" />
                    <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg" />
                </q-carousel>
            </div>
        </q-card>

    </q-page>
</template>
  
<script>
import { defineComponent } from 'vue'
import { ref } from 'vue'

export default defineComponent({
    name: 'IndexPage',

    data() {
        return {
            slide: ref(1),
            rows,
            heads: [
                { content: "Total Inventary" },
                { content: "Total Active" },
                { content: "Total Cancel" },
                { content: "Total Sales" },
            ],
            nums: [
                { content: "3,930" },
                { content: "1,268" },
                { content: "170" },
                { content: "28,060" },

            ],
        }
    }
});
const rows = [
    {
        name: 'Frozen Yogurt',
        calories: 159,
        fat: 6.0,
        carbs: 24,
        protein: 4.0,
        sodium: 87,
        calcium: '14%',
        iron: '1%'
    },
    {
        name: 'Ice cream sandwich',
        calories: 237,
        fat: 9.0,
        carbs: 37,
        protein: 4.3,
        sodium: 129,
        calcium: '8%',
        iron: '1%'
    },
    {
        name: 'Eclair',
        calories: 262,
        fat: 16.0,
        carbs: 23,
        protein: 6.0,
        sodium: 337,
        calcium: '6%',
        iron: '7%'
    },
    {
        name: 'Cupcake',
        calories: 305,
        fat: 3.7,
        carbs: 67,
        protein: 4.3,
        sodium: 413,
        calcium: '3%',
        iron: '8%'
    },
    {
        name: 'Gingerbread',
        calories: 356,
        fat: 16.0,
        carbs: 49,
        protein: 3.9,
        sodium: 327,
        calcium: '7%',
        iron: '16%'
    },
    {
        name: 'Jelly bean',
        calories: 375,
        fat: 0.0,
        carbs: 94,
        protein: 0.0,
        sodium: 50,
        calcium: '0%',
        iron: '0%'
    },
    {
        name: 'Lollipop',
        calories: 392,
        fat: 0.2,
        carbs: 98,
        protein: 0,
        sodium: 38,
        calcium: '0%',
        iron: '2%'
    },
    {
        name: 'Honeycomb',
        calories: 408,
        fat: 3.2,
        carbs: 87,
        protein: 6.5,
        sodium: 562,
        calcium: '0%',
        iron: '45%'
    },
    {
        name: 'Donut',
        calories: 452,
        fat: 25.0,
        carbs: 51,
        protein: 4.9,
        sodium: 326,
        calcium: '2%',
        iron: '22%'
    },
    {
        name: 'KitKat',
        calories: 518,
        fat: 26.0,
        carbs: 65,
        protein: 7,
        sodium: 54,
        calcium: '12%',
        iron: '6%'
    }
]
</script>
  