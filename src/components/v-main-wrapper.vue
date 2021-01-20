<template>
    <div class="v-main-wrapper">
        <h1>Catalog</h1>
        <keep-alive>
            <router-view>

            </router-view>
        </keep-alive>

<!--        <vCatalog/>-->
<!--        <vCart-->
<!--            v-if="CART.length"-->
<!--            :cart_data="CART"-->
<!--        />-->
    </div>
</template>

<script>
    // import vCatalog from './v-catalog';
    // import vCart from './v-cart';
    //import {mapGetters} from 'vuex';
    export default {
        name: "v-main-wrapper",
        // components:{
        //     vCatalog, vCart
        // },
        data(){
            return{

            }
        },
        // computed:{
        //     ...mapGetters([
        //         'CART'
        //     ])
        // }
    }
</script>

<style>
    .v-main-wrapper{
        max-width: 900px;
        margin: 0 auto;
    }
</style>