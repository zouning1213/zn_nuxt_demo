<template>
  <div class="container">
    <div> 
      <ul>
          <li v-for="(item,index) in list" :key="index">
              <nuxt-link :to="'/goods_detail/'+item.id">
                {{item.name+'/goods_detail/'+item.id}}
              </nuxt-link>
          </li>
      </ul>
    </div>
  </div>
</template>

<script> 

export default { 
    data(){
        return{
            list :[
                {id:'001',name:"张三"}, 
                {id:'002',name:"张四"}, 
                {id:'003',name:"张五"}, 
            ]
               
        }
    }
}
</script>

<style> 
</style>
