<script>
  export default {
    data() {
      return {
        name: 'John Doe',
        status: 'pending',
        tasks: ['Task 1', 'Task 2', 'Task 3'],
        Link: 'https://www.google.com/'
      };
    },
    methods: {
      toggleStatus() {
        if (this.status === 'active') {
          this.status = 'pending';
        } else if (this.status === 'pending') {
          this.status = 'inactive'
        } else {
          this.status = 'active'
        }
      }
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
  <a :href="Link">Click for Google</a>
  <button @click="toggleStatus">Change Status</button>
</template>