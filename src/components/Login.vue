<script setup>
defineProps({
  
})
</script>

<template>

  <div class="main">
  

    <form @submit.prevent="save" class="login">
      <h2>College Registration Course</h2>
      <h4>Login</h4>
        <div class="form-group">
          <label for="exampleInputEmail1">Email <Address></Address></label>
          <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Enter Email" aria-describedby="emailHelp" >
          
        </div>
        <div class="form-group">
          <label for="exampleInputPassword1">Password</label>
          <input type="password" class="form-control" placeholder="Enter Password" id="exampleInputPassword1" >
        </div>
        <div class="form-group"></div>   
        <button type="submit" class="btn btn-primary">Enter System</button>
        
  </form>
</div>
</template>

<style scoped>
.login{
  border-style:solid;
  border-width: 1px;
  padding: 30px;
  width: 50vw;
  margin-left: 15%;

}
.form-group{
  padding-top: 20px;
}
/* h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
} */
</style>
