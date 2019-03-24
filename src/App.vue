<template>
  <div>
    <SearchBar @termChange="onTermChange"></SearchBar>
  </div>
</template>

<script>
  import axios from 'axios';
  import SearchBar from './components/SearchBar';
  const API_KEY = 'AIzaSyDG8-7JlzWc26LkW3NwFLqP3rrE7P9cJVE';

  export default {
    name: 'App',
    components: {
      SearchBar
    },
    methods: {
      onTermChange(searchTerm) {
        axios.get('https://www.googleapis.com/youtube/v3/search', {
          params: {
            key: API_KEY,
            type: 'video',
            part: 'snippet',
            q: searchTerm
          }
        }).then(response => console.log(response));
      }
    }
  };
</script>
