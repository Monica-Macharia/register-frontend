<script setup>

import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>

<div class="main">
  <h2>Register Course</h2>

  
  <form @submit.prevent="save">
        <div class="form-group">
          <label for="exampleInputEmail1">Course Name</label>
          <input type="text" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" >
          
        </div>
        <div class="form-group">
          <label for="exampleInputPassword1">Teacher Name</label>
          <input type="text" class="form-control" id="exampleInputPassword1" >
        </div>
        <div class="form-group">
          <label for="exampleInputPassword2">Total of Hours</label>
          <input type="number" class="form-control" id="exampleInputPassword2" >
        </div>
       
        <button type="submit" class="btn btn-primary">Register</button>
  </form>

  <br />
  <table class="table">
  <thead>
    <tr>
      <th scope="col">Unique Code</th>
      <th scope="col">Course Name</th>
      <th scope="col">Teacher Name</th>
      <th scope="col">Total of Hours</th>
      <th scope="col">Select</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
      <td></td>
      <td><button type="submit" class="btn btn-primary">Select</button></td>
    </tr>
   
  </tbody>
</table>
</div>

</template>
