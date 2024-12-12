<script>
  export default {
    setup() {
      const name = 'John Doe';
      const status = 'active';
      const tasks = ['Task One', 'Task Two', 'Task Three'];
      
      const toggleStatus = () => {
        if (this.status === 'active') {
          this.status = 'pending';
        } else if (this.status === 'pending') {
          this.status = 'inactive'
        } else {
          this.status = 'active'
        }
      };
    }
  };
</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">user is pending</p>
  <p v-else>user is inactive</p>
  <h3>Tasks:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">
      {{ task }}
    </li>
  </ul>
</template>