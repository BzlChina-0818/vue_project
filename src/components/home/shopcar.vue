<template>
    <div>
        购物车
    </div>
</template>

<script>
import {getCookie} from '../../until/decode.js'
export default {
    data(){
        return {

        }
    },
   
    beforeRouteEnter (to, from, next) {
          let islogin =getCookie('token')
           if(islogin){
               next()
           }else{
              next({name:"login"})
           }
    }
}
</script>

<style>

</style>
