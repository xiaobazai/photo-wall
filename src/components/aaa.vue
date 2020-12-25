<template>
    <div class="box">
<h4>摄影社区热门小镇</h4>
<ul>
    <li v-for="(item, index) in cityLists" :key="index" >
        <img :src="item.src" alt="">
        <div class="content">
            <p class="title">{{item.title}}</p>
            <p class="grey mt">成员：{{item.team}}</p>
            <p class="grey">作品：{{item.zp}}</p>
        </div>
    </li>
</ul>
    </div>
</template>

<script>

    export default {
        props:['cityLists']
    }
</script>

<style  scoped>
*{
  padding: 0;
  margin: 0;
  list-style: none;
}
.box{
    width: 660px;
    border: 1px solid #ccc;
    margin:  20px auto;
    padding: 10px ;
}
.title{
    color: rgb(35, 185, 223);
}
.content{
    padding: 0px 15px;
}
h4{
    margin-left: 20px;
}
ul{
    width: 100%;
    display: flex;
    flex-wrap: wrap;
}
li{
    display: flex;
    margin: 10px 20px;
}
li img{
    padding: 3px 3px;
    border: 1px solid #ccc;
    border-radius: 4px;
    margin: 3px 2px;
}
.grey{
    color: #a5a0a0;

}
.mt{
    margin-top: 5px;
}
</style>