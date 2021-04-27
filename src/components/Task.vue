<template>
<div @dblclick="$emit('toggleReminder', task.id)" :class="[task.reminder ? 'reminder' : ' ', 'task']">
     <h3>
        {{task.text}}
        <i @click="$emit('deleteTask', task.id)" class="fas fa-times"></i>
    </h3>
    <p>{{ task.day }}</p>
</div>
   
</template>

<script>
export default  {
    name: 'Task',
    props: {
        task: Object
    }
    
}
</script>
<style scopeed>
.fas {
  color: red;
}
.task {
  background: #f4f4f47c;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
}
.task.reminder {
  border-left: 5px solid green;
}
.task h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
