<template>
  <h2>List data from web site</h2>
  <SinglePost 
  v-for="(item,index) in data"
  
  
  :name="item.Moviename" 
  :released="item.releaseday" 
  :introduction="item.description" 
  :collection="item.collections"
  :position="index"
  :imagespic="item.images"
  v-on:delecteCard="delecteCard"
  />
  
  
  </template>
  <script setup>
  import SinglePost from './components/SinglePost.vue';
import {ref} from 'vue';
let data=ref([
  {
    Moviename:"jaishihaa",
    releaseday:"21-11-2024",
    description:"Dive into the neon-lit streets of  a neo-noir film that combines elements of mystery and science fiction. Follow a detective as he unravels a web of conspiracy in a futuristic city.",
    collections:213263763278 ,
    images:"https://static.toiimg.com/thumb/msid-103656989,width-1280,height-720,resizemode-4/103656989.jpg"
    





},

{
    Moviename:"guntur-karam",
    releaseday:"12-09-2024",
    description:"unravels the secrets of a mysterious city. Join the adventure as a detective tries to solve a series of perplexing crimes, revealing the hidden layers of Guntur-Karam.",
    collections:287 ,
    images:"https://static.toiimg.com/thumb/msid-103656989,width-1280,height-720,resizemode-4/103656989.jpg"
    





},

{
Moviename:"Inception Reimagined",
    releaseday:"14-12-2024",
    description:"A mind-bending heist movie directed by visionary filmmaker Christopher Nolan. Dive into dreams within dreams as a skilled thief navigates the complexity of the subconscious.",
    collections:287  ,
    images:"https://static.toiimg.com/thumb/msid-103656989,width-1280,height-720,resizemode-4/103656989.jpg"
    





},

{
Moviename:"salaar",
    releaseday:"14-12-2024",
    description:" unfolds the gripping tale of a lone warrior on a quest for justice. With intense action sequences and a powerful narrative, this film explores the essence of honor and sacrifice.",
    collections:287  ,
    images:"https://static.toiimg.com/thumb/msid-103656989,width-1280,height-720,resizemode-4/103656989.jpg"
    





},
{
Moviename:"The Elysian Chronicles",
    releaseday:"14-12-2024",
    description:"Enter the mythical world of  where ancient prophecies and mystical creatures come to life. A group of heroes must unite to save their realm from an impending darkness.",
    collections:287  ,
    images:"https://static.toiimg.com/thumb/msid-103656989,width-1280,height-720,resizemode-4/103656989.jpg"
    





},{
Moviename:"Ocean's Riddle",
    releaseday:"14-12-2024",
    description:"is a suspenseful thriller that takes you into the world of high-stakes heists. A group of skilled individuals must outsmart the authorities and navigate intricate plans to achieve the ultimate score. ",
    collections:287  ,
    images:"https://static.toiimg.com/thumb/msid-103656989,width-1280,height-720,resizemode-4/103656989.jpg"
    





}




])

function delecteCard(position){
  data.value.splice(position,1)
}
</script>
<style scoped>
  h2 {
    text-align: center;
    color: #353434;
  }

  </style>
