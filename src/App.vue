<template>
  <div>
    <SearchBar @termChange="onTermChange"></SearchBar>
  </div>
</template>

<script>
  import SearchBar from './components/SearchBar';
  const API_KEY = 'AIzaSyDG8-7JlzWc26LkW3NwFLqP3rrE7P9cJVE';

  export default {
    name: 'App',
    components: {
      SearchBar
    },
    methods: {
      onTermChange(searchTerm) {
        console.log(searchTerm);
      }
    }
  };
</script>
