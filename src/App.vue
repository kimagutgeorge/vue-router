<template>
 <div id="nav">
    <RouterLink to="/" class="btn">Home</RouterLink>
    <RouterLink :to="{ name: 'About' }" class="btn">About</RouterLink>
    <RouterLink :to="{ name: 'Jobs' }" class="btn">Jobs</RouterLink>
    <br><br>
    <button @click="redirect" >Redidrect</button>
    <button @click="back" >Go back</button>
    <button @click="forward" >Go forward</button>
 </div>
<RouterView/>
</template>

<script>
  export default {
    methods: {
      redirect(){
        this.$router.push({ name:'home' })
      },
      back(){
        this.$router.go(-1)
      },
      forward(){
        this.$router.go(1)
      }
    }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.btn{
  margin:0 5px;
  padding:5px 10px;
  font-weight: bold;
  text-decoration: none;
  color:#333;
  border-radius: 5px;
}
.btn.router-link-active{
  background-color: rgb(217, 67, 67);
  color:white;
}
button{
  margin:0 10px;
  padding:10px;
  border:none;
  border-radius: 4px;
  cursor: pointer;
}

</style>
