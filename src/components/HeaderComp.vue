<template>
   <div class="nav">
            <router-link to="/">Home</router-link>
            <router-link to="/add-r">Add Restaurant</router-link>
            <router-link to="update-r">Update Restaurant</router-link>
            <a v-on:click="logout" href="#">Logout</a>
   </div>
</template>

<script>
export default{
        name:'HeaderComp',
        methods:{
            logout(){
                    localStorage.clear();
                    this.$router.push({name:'LoginPage'})
            }
        }
}
</script>

<style>
.nav{
    background-color: #333;
    overflow: hidden;
}
.nav a {
  float: left;
  color: #f2f2f2f2;
  padding: 14px 16px;
  font-size: 17px;
  text-decoration: none;
  text-align: center;
  margin-right: 5px;
}
.nav a:hover{
    background: #ddd;
    color:#333
}
</style>