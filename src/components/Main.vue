<template>

<div class="main">
  <h2>Main Panel</h2>
  

      <form>
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
          
            <button type="submit" class="btn btn-primary">Edit</button>
            
            <button type="submit" class="btn btn-primary">Remove</button>
            <button type="submit" class="btn btn-primary">Cancel</button>
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

<style scoped>
/* .item {
  margin-top: 2rem;
  display: flex;
}

.details {
  flex: 1;
  margin-left: 1rem;
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  width: 32px;
  height: 32px;
  color: var(--color-text);
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

@media (min-width: 1024px) {
  .item {
    margin-top: 0;
    padding: 0.4rem 0 1rem calc(var(--section-gap) / 2);
  }

  i {
    top: calc(50% - 25px);
    left: -26px;
    position: absolute;
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px;
    width: 50px;
    height: 50px;
  }

  .item:before {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:after {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }
} --> */
</style>
