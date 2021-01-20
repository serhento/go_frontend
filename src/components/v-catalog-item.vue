<template>
    <div class="v-catalog-item">
        <img class="v-catalog-item__image" :src="require('../assets/images/' + product_data.image)" alt="img">
        <router-link :to="{name: 'test', params: {item_data: product_data, id: product_data.id}}">
            <p
                    class="v-catalog-item__name"
                    @click="itemId"
            >{{product_data.name}}</p>
        </router-link>
        <p class="v-catalog-item__price">Price: {{product_data.price}} P.</p>
        <button class="v-catalog-item__add_to_cart_btn btn" @click="addToCart">Add to cart</button>
    </div>
</template>

<script>
    export default {
        name: "v-catalog-item",
        props:{
            product_data:{
                type: Object,
                default(){
                    return {}
                }
            }
        },
        methods:{
            addToCart(){
                this.$emit('addToCart',this.product_data);
            },
            itemId(){
                this.$emit('itemId',this.product_data.id);
            }
            // qweqq(){
            //     this.$router.push('/'+this.product_data.id)
            // }
        }
    }
</script>

<style lang="scss">
    .v-catalog-item{
        flex-basis: 25%;
        box-shadow: 0 0 8px 0 #e0e0e0;
        padding: 16px;
        margin: 16px;

        &__image{
            width: 100px;
        }

        &__add_to_cart_btn{
            cursor: pointer;
        }
    }
</style>