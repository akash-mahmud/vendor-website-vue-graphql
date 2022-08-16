<template>

<div class="container mx-auto">

<div class="grid  place-items-center" v-for="post in  posts.nodes" :key="post.id">

<a href="#" class="mt-2 block p-6 max-w-sm bg-white rounded-lg border border-gray-200 shadow-md hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{{post.title}}</h5>
    <!-- <p class="font-normal text-gray-700 dark:text-gray-400">Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.</p> -->
</a>


</div>
</div>



</template>

<script>

import gql from 'graphql-tag'
export default {
  
  // name: 'IndexPage' , 
    apollo : {
    posts : gql`query getPosts{
      posts  {
nodes{
        title
      slug
      id
}
      }
    }`
  }
}



</script>
