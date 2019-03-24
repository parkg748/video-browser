<template>
  <ul>
    VideoList
    <VideoListItem></VideoListItem>
  </ul>
</template>

<script>
  import VideoListItem from './VideoListItem';

  export default {
    name: 'VideoList',
    components: {
      VideoListItem,
    },
    props: ['videos']
  }
</script>

<style>
</style>
