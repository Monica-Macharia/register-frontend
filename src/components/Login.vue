<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  
  <div class="main">
  <h2>College Registration Course</h2>
  <h4>Login</h4>

    <form>
        <div class="form-group">
          <label for="exampleInputEmail1">Email <Address></Address></label>
          <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Enter Email" aria-describedby="emailHelp" >
          
        </div>
        <div class="form-group">
          <label for="exampleInputPassword1">Password</label>
          <input type="password" class="form-control" placeholder="Enter Password" id="exampleInputPassword1" >
        </div>
             
        <button type="submit" class="btn btn-primary">Enter System</button>
        
  </form>
</div>
</template>

<style scoped>
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
