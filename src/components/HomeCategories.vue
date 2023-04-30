<template>
    <q-card flat class="q-py-sm q-px-lg column items-center justify-center">
        <div><q-avatar size="70px" color="yellow-9">
                <img :src=image>
            </q-avatar></div>
        <div>{{ title }}</div>

    </q-card>
</template>
<script>
import { defineComponent } from 'vue'
export default defineComponent({
    name: 'HomeCategories',
    props: {
        title: {
            type: String,
            required: true
        },

        link: {
            type: String,
            default: '#'
        },

        image: {
            type: String,
            default: ''
        }
    }
})
</script>