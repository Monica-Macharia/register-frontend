<script>

//for state management-COMPOSITION API
  import {ref, onMounted } from 'vue';

  export default {
    setup() {
      const courseName = ref('');
      const teacherName = ref('');
      const totalHours = ref(0);
      const courses = ref([]);

      //saving input values from form
      const save = () => {
        const newCourse = {
          courseName: courseName.value,
          teacherName: teacherName.value,
          totalHours: totalHours.value,
        };

        //persist the new data to the database using fetch()
        fetch('', {
          method: 'POST',
          headers: {
            'Content-type': 'application/json',
          },
          body:JSON.stringify(newCourse),
        })
        .then(res => {
          if(res.ok) {
            courses.value.push(newCourse);
            //reset the form
            courseName.value="";
            teacherName.value="";
            totalHours.value=0;
          }else{
            console.error("Operation failed");
          }
        })
        .catch(error =>{
          console.error(error);
        });
      

      };

      //to post the acquired data to the table right next to the form
      //fetch the modified array straight from the database and render on page load

      onMounted(() => {
        fetch('')
        .then(res =>{
          if(res.ok){
            return res.json();
          }else{
            console.log("failed to fetch")
          }
        })
        .then(data => {
          courses.value = data;
        })
        .catch(error => {
          console.log(error);
        });
      });
      return {
        courseName,
        teacherName,
        totalHours,
        courses,
        save,
      };
      
    },
  }

</script>

<template>

<div class="main">
  <h2>Register Course</h2>

  
  <form @submit.prevent="save">
        <div class="form-group">
          <label for="courseName">Course Name</label>
          <input type="text" class="form-control" v-model="courseName" id="courseName" aria-describedby="emailHelp" >
          
        </div>
        <div class="form-group">
          <label for="teacherName">Teacher Name</label>
          <input type="text" class="form-control" v-model="teacherName" id="teacherName" >
        </div>
        <div class="form-group">
          <label for="totalHours">Total of Hours</label>
          <input type="number" class="form-control" v-model="totalHours" id="totalHours" >
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
    <tr v-for="(course, index) in courses" :key="index">
      <th scope="row">{{ course.id }}</th>
      <td>{{ course.courseName }}</td>
      <td>{{ course.teacherName }}</td>
      <td>{{ course.totalHours }}</td>
   
      <td><button type="submit" class="btn btn-primary">Select</button></td>
    </tr>
   
  </tbody>
</table>
</div>

</template>

