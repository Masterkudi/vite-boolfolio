<script>
import axios from 'axios';

	export default {
    data() {
      return {
        projects: [],
        pagination: {}
      };
    },
    methods: {
      fetchData() {
        axios.get('http://127.0.0.1:8000/api/projects')
          .then((response) => {
            console.log(response);
          })
      }
    },
    mounted() {
      this.fetchData();
    }
	};
</script>

<template>
  <h1>Hello from Vue!</h1>
</template>