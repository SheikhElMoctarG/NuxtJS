<template>
  <div class="app">
    <h4> {{$route.params.id}} </h4>
  </div>
</template>
<script>
export default {
  validate({params}){
    return !isNaN(params.id)
  }
}
</script>
