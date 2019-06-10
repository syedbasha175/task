<template>
<div>

<h4 >Username:<input type="text"  v-model="username" id="txt"/></h4>
<h4 >Mail ID:<input type="text"  v-model="usermail" id="mail"/></h4>

<input type="submit" value="click" v-on:click="passvalues();"/>


</div>
</template>
<script>

export default {
     
data() {
  
    return {
      
            username: "",
            usermail:"",
          
        }
    },
    methods:{
          passvalues()  {
  this.$router.push({ path: '/mycomp?name='+this.username } );
}
    }
  
}
        //  function passvalues(){
        // {
        //     var firstname=document.getElementById("txt").value;
        //     localStorge.setItem("textvalue",firstname);
        //     return false;
        // }

</script>