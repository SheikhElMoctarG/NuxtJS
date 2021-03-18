<template>
  <div class="index">
    <div  v-for="item in per" :key="item.id">
    <v-card
    class="mx-auto"
    max-width="344"
  >
    <v-card-text>
      <h1> {{item.name}} </h1>
      <div class="text--primary">
        he has {{item.age}} year,
        working in {{item.department}}
      </div>
    </v-card-text>

  </v-card>
    </div>
  </div>
</template>
<script>
import axios from 'axios'
export default {
  data(){
    return{
    per: []
    }
  },
  created(){
     axios.get('https://api-generation.herokuapp.com/').then(res =>{
        this.per = res.data
    })
  }
}
</script>
<style>
.mx-auto{
  text-align: center;
}
</style>
