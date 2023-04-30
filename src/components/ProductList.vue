<template>
    <q-card flat class="q-py-sm q-px-lg" style="width: 180px">
        <q-img fit="contain" ratio="1" :src="image" />
        <div class="column full-width items-center">
            <div class="text-weight-bold q-pa-sm">{{ title }}</div>
            <div class="text-green q-pa-sm ">{{ price }}</div>
            <div class="text-grey-8">{{ caption }}</div>
        </div>


    </q-card>


    <!-- <diV style="height:320px; width: 250px">
            <q-img src="https://rukminim1.flixcart.com/fk-p-flap/464/708/image/3f412f62bc981f69.jpeg?q=70"
                style="height:320px; max-width: 250px" />
        </diV> -->
</template>
<script>
import { defineComponent } from 'vue'
export default defineComponent({
    name: 'ProductList',
    props: {
        image: {
            type: String,
            default: ''
        },
        title: {
            type: String,
            required: true
        },
        price: {
            type: String,
            default: ''
        },
        caption: {
            type: String,
            default: ''
        },
        link: {
            type: String,
            default: '#'
        },
    }


})

</script>
