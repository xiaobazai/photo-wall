<template>
  <div>
    <aaa :cityLists='cityLists' />
  </div>
</template>

<script>
import aaa from './components/aaa'
import axios from "axios"
  export default {
    components:{aaa,},
    data() {
      return {
        cityLists:[]
      }
    },
    created() {
      axios.get('https://www.fastmock.site/mock/7420c344e74214adfb9a88ee8984b886/xiao/lisss', )
      .then((res)=> {
        console.log(res.data);
        this.cityLists=res.data
        console.log(this.cityLists);
      })
      
    },
  }
</script>

<style  scoped>
*{
  padding: 0;
  margin: 0;
  list-style: none;
}
</style>