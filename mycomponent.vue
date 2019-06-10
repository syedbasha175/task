<template>
<div>
<span  v-model="name">Username is {{name}}</span>

</div>
</template>

<script>

export default {
 
  data () {
    return {
      name : this.$route.query.name
    }
     
    }
  }
</script>