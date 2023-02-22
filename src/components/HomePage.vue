<template>
  <HeaderComp />
    <h1>Hello {{name}}, Welcome on Home Page</h1>
</template>

<script>
import HeaderComp from './HeaderComp.vue'
export default{
    name:'HomePage',
    data(){
      return{
            name:''
          }
    },
    components:{
      HeaderComp
    },
    mounted()
    {
              let user= localStorage.getItem('user-info');
              this.name= JSON.parse(user).name;
              if(!user)
              {
                this.$router.push({name:'SignUp'})
              }
    }
}
</script>