<template>
    <div class="v-test">
<!--        <h1>Catalog</h1>-->
        <router-link :to="{name: 'catalog'}">
            <div class="v-catalog__link_to_cart">Back to catalog</div>
        </router-link>
        <vCatalogItem :product_data="item_data"/>
    </div>
</template>

<script>
    import vCatalogItem from './v-catalog-item'
    export default {
        name: "v-test",
        components:{
            vCatalogItem
        },
        props:{
            item_data:{
                type: Object,
                default(){
                    return {}
                }
            },
            id:{}
        }
    }
</script>

<style lang="scss">

</style>