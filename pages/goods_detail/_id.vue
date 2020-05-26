<template>
  <div class="container">
    <div> 
      isdetails 
      <h1>{{$route.params.id}}</h1>
      {{detail}}
    </div>
  </div>
</template>

<script> 
import axios from "axios"
export default { 
    async asyncData() { 
        // return axios.get("/data/test.json").then((res)=>{
        //      return {
        //          detail:res.data
        //      }
        //  })
        let res = await axios.get("/data/test.json")
        return{
            detail:res.data
        }
     }
}
</script>

<style> 
</style>
