<template>
    <div class="container">

        <ul>
            <li><div><img :src="imagespic"/></div></li>
              <li>Moviename:  {{ name }}</li>
               <li>releasedday:  {{ released }}</li>
               <li>description: <span>{{ introduction }}</span></li>
               <li>{{ collection }}</li>    
               <li>{{ imagespic }}</li> 
              


        </ul>
        <button @click="$emit('delecteCard',position)">delete the inform</button>
    </div>
</template>
<script setup>
defineProps({
    name:String,
    released:String,
    introduction:String,
    collection:Number,
    position:Number,
    imagespic:String



           





})

</script>
<style scoped>
.container {
  display: grid;
  grid-template-columns: 1fr;
  gap: 10px;
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
    margin-bottom: 10px;
}
li div {
    text-align: center;
}
img {
  border-radius: 5px;
  margin-top: 10px;
  height: 300px;
  justify-content: center;
  
  text-align: center;
  margin:0 auto;
}

button {
  grid-column: span 2; /* Button spans two columns */
  background-color: #dc3545;
  color: #fff;
  border: none;
  padding: 8px 12px;
  cursor: pointer;
  border-radius: 3px;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #c82333;
}

span {
  font-weight: bold;
  display: block;
}
</style>

