<template>
  <HeaderComp />
    <h1>Hello User, Welcome on Update Restaurant Page</h1>
</template>

<script>
import HeaderComp from './HeaderComp.vue'
export default{
    name:'UpdateR',
    components:{
      HeaderComp
    },
    mounted()
    {
              let user= localStorage.getItem('user-info');
              if(!user)
              {
                this.$router.push({name:'SignUp'})
              }
    }
}
</script>