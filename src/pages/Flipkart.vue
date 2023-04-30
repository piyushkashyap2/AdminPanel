<template>
    <div class="row  items-center scroll no-wrap q-px-xl">
        <HomeCategories v-for="link in HomeCategories" :key="link.title" v-bind="link" />
    </div>
    <q-card class="q-pa-md">

        <q-carousel style="height: 300px;" animated v-model="slide" arrows navigation infinite>
            <q-carousel-slide :name="1"
                img-src="https://rukminim1.flixcart.com/fk-p-flap/844/140/image/a473e0c2ff5779e1.jpg?q=50" />
            <q-carousel-slide :name="2"
                img-src="https://rukminim1.flixcart.com/flap/50/50/image/75a15c3e19c3f7de.jpg?q=50" />
            <q-carousel-slide :name="3"
                img-src="https://rukminim1.flixcart.com/fk-p-flap/50/50/image/9e47728b9e93ad32.png?q=50" />
            <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg" />
        </q-carousel>
    </q-card>
    <q-card>
        <q-img src="https://rukminim1.flixcart.com/fk-p-flap/100/100/image/31bc5f75424dd33c.jpg?q=50" />
    </q-card>
    <div class="row full-width q-my-sm">

        <div class="column items-center justify-center" style="height: 320px; width: 250px">
            <div class="text-h4 q-py-xl">Top Offers</div>
            <q-btn label="View All" class="q-px-md q-my-sm" align="between" color="blue" text-color="white" unelevated
                @click=""></q-btn>
            <div class="bg-blue " style="height:120px; width: 250px"></div>
        </div>
        <div class="row scroll col">
            <div class="row no-wrap">
                <ProductList v-for="link in ProductList" :key="link.title" v-bind="link" />
            </div>

        </div>



    </div>
    <div class="row full-width q-my-sm">

        <div class="column items-center justify-center" style="height: 320px; width: 250px">
            <div class="text-h4 q-py-xl">Top Offers</div>
            <q-btn label="View All" class="q-px-md q-my-sm" align="between" color="blue" text-color="white" unelevated
                @click=""></q-btn>
            <div class="bg-blue " style="height:120px; width: 250px"></div>
        </div>
        <div class="row scroll col">
            <div class="row no-wrap">
                <ProductList v-for="link in ProductList" :key="link.title" v-bind="link" />
            </div>

        </div>



    </div>
    <div class="row full-width q-my-sm">

        <div class="column items-center justify-center" style="height: 320px; width: 250px">
            <div class="text-h4 q-py-xl">Top Offers</div>
            <q-btn label="View All" class="q-px-md q-my-sm" align="between" color="blue" text-color="white" unelevated
                @click=""></q-btn>
            <div class="bg-blue " style="height:120px; width: 250px"></div>
        </div>
        <div class="row scroll col">
            <div class="row no-wrap">
                <ProductList v-for="link in ProductList" :key="link.title" v-bind="link" />
            </div>

        </div>



    </div>
</template>
<script>
import HomeCategories from 'src/components/HomeCategories.vue';
import ProductList from 'src/components/ProductList.vue';
import { ref } from 'vue'
export default {

    data() {
        return {
            slide: ref(1),
            HomeCategories: categoriesList,
            ProductList: itemsList,
        };
    },
    components: { HomeCategories, ProductList },
}
const categoriesList = [
    {
        title: 'Top Offers',
        image: 'https://rukminim1.flixcart.com/fk-p-flap/128/128/image/1350e22cff9663e7.png?q=100',
        link: ''

    },
    {
        title: 'Mobiles & Tablets',
        image: 'https://rukminim1.flixcart.com/fk-p-flap/128/128/image/d64cae0f8081256a.png?q=100',
        link: ''
    },
    {
        title: 'Elecronics',
        image: 'https://rukminim1.flixcart.com/fk-p-flap/128/128/image/7dbcda527b648814.png?q=100',
        link: ''
    },
    {
        title: 'TVs & Appliances ',
        image: 'https://rukminim1.flixcart.com/fk-p-flap/128/128/image/e29a070388d534a5.png?q=100',
        link: ''
    },
    {
        title: 'Fashion',
        image: 'https://rukminim1.flixcart.com/fk-p-flap/128/128/image/d44ffc537ed6e241.png?q=100',
        link: ''
    },
    {
        title: 'Beauty',
        image: 'https://rukminim1.flixcart.com/fk-p-flap/128/128/image/994a83c90019fb5f.png?q=100',
        link: ''
    },
    {
        title: 'Home & Furniture',
        image: 'https://rukminim1.flixcart.com/fk-p-flap/128/128/image/d300931a0fd1c17e.png?q=100',
        link: ''
    },
    {
        title: 'Flights',
        image: 'https://rukminim1.flixcart.com/fk-p-flap/128/128/image/2dac2decff60c650.png?q=100',
        link: ''
    },
    {
        title: 'Grocery',
        image: 'https://rukminim1.flixcart.com/fk-p-flap/128/128/image/46376ceed3448aff.png?q=100',
        link: ''
    },
]
const itemsList = [
    {
        image: 'https://rukminim1.flixcart.com/image/200/200/kokdci80/dslr-camera/v/e/x/z-24-200mm-z5-nikon-original-imag2zuekuxgxsgg.jpeg?q=70',
        title: 'Top Mirrorless cameras',
        price: 'From 10,000',
        caption: 'Canon, Sony'
    },
    {
        image: 'https://rukminim1.flixcart.com/image/200/200/printer/j/j/y/hp-laserjet-m1005-multifunction-original-imadxhzpeb9qbrfg.jpeg?q=70',
        title: 'Printers',
        price: 'From 10,000',
        caption: 'Brothers'
    },
    {
        image: 'https://rukminim1.flixcart.com/image/200/200/l4x2rgw0/monitor/n/y/y/q24i-20-full-hd-23-8-66eegac3in-lenovo-original-imagfpgxzsk8ef26.jpeg?q=70',
        title: 'Top Mirrorless cameras',
        price: 'From 10,000',
        caption: 'Canon, Sony'
    },
    {
        image: 'https://rukminim1.flixcart.com/image/200/200/l55nekw0/monitor/j/m/b/vz24ehe-full-hd-23-8-90lm07c3-b01410-asus-original-imagfwed5g2s2d7y.jpeg?q=70',
        title: 'Top Mirrorless cameras',
        price: 'From 10,000',
        caption: 'Canon, Sony'
    },
    {
        image: 'https://rukminim1.flixcart.com/image/200/200/l55nekw0/monitor/j/m/b/vz24ehe-full-hd-23-8-90lm07c3-b01410-asus-original-imagfwed5g2s2d7y.jpeg?q=70',
        title: 'Top Mirrorless cameras',
        price: 'From 10,000',
        caption: 'Canon, Sony'
    },
    {
        image: 'https://rukminim1.flixcart.com/image/200/200/l55nekw0/monitor/j/m/b/vz24ehe-full-hd-23-8-90lm07c3-b01410-asus-original-imagfwed5g2s2d7y.jpeg?q=70',
        title: 'Top Mirrorless cameras',
        price: 'From 10,000',
        caption: 'Canon, Sony'
    },
    {
        image: 'https://rukminim1.flixcart.com/image/200/200/l55nekw0/monitor/j/m/b/vz24ehe-full-hd-23-8-90lm07c3-b01410-asus-original-imagfwed5g2s2d7y.jpeg?q=70',
        title: 'Top Mirrorless cameras',
        price: 'From 10,000',
        caption: 'Canon, Sony'
    },
    {
        image: 'https://rukminim1.flixcart.com/image/200/200/l55nekw0/monitor/j/m/b/vz24ehe-full-hd-23-8-90lm07c3-b01410-asus-original-imagfwed5g2s2d7y.jpeg?q=70',
        title: 'Top Mirrorless cameras',
        price: 'From 10,000',
        caption: 'Canon, Sony'
    },
]

</script>