<template>
    <div class="cart-item">
        <router-link :to="{path:'/detail',query:{productId: item.product.id}}">
            <img :src="'http://47.107.62.230:9080/repo/tb/'+item.rela[0].filePath">
            <div class="desc-block">
                    <div class="product-name">{{item.product.productName}}</div>
                <div class="buy-num" v-if="show_price"><strong>{{item.product.productPrice}}X1</strong></div>
            </div>
        </router-link>
    </div>
</template>


<script>
    export default{
        name: 'HistoryItem',
        components:{
        },
        props:{
            item:{
                type:Object,
            },
            show_price:{
                type: Boolean,
                default: true
            }
        }
    }
</script>

<style scoped>
    .cart-item img{
        width:200px;
        height:300px;
    }
    .desc-block{
        vertical-align: top;
        /*padding: 0 15px;*/
    }
    a{
        text-decoration: none;
        color:black;
    }
    .desc-block .product-name{
        /*width: 295px;*/
        /*display: inline-block;*/
    }
    .desc-block .buy-num{
        /*display:inline-block;*/
        /*float:right;*/
    }
    .cart-item{
        text-align: left;
        display:inline-block;
        width:200px;
        vertical-align: top;
        padding:10px;
    }
</style>
