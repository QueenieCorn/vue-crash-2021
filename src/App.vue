<template>
  <div class="container">
   <Header title="Task Tracker" />
   <Tasks @delete-task="deleteTask" :tasks="tasks" />
  </div>
</template>

<script> 
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header'
import Tasks from './components/Tasks' 

export default {
  name: 'App',
  components: {
    Header,
    Tasks,
  },
  data() {
    return{
      task: [],
    }
  },
  methods :{
    deleteTask(id){
      // console.log(id);
      this.tasks = this.tasks.filter((task) => task.id !== id )
    }
  },
  created() {
    this.tasks = [
      {
        id: 1,
        text: 'Doctors Appointment',
        day: 'March 1st at 2:30pm',
        reminder: true,
      },
      {
        id: 2,
        text: 'Meeting at School',
        day: 'March 3rd at 1:30pm',
        reminder: true,
      },
      {
        id: 3,
        text: 'Food Shopping',
        day: 'March 3rd at 11:00am',
        reminder: false,
      },
    ]
  }
}
</script>

<style>

*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body{
  font-family: 'Poppins, sans-serif';
}

.container{
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}

.btn{
  display: inline-block;
  background: #000;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus{
  outline:none;
}
/* 
.green{
  background-color: #008000;
} */

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
