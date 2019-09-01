<template>
  <div style="margin-bottom:20px;padding:50px;">
    <div class="tabs">
      <span 
      v-for="(item,index) in ['东','南','西','北']"
      :key="index"
      @click="handleClick(index)"
      :class="{active:current === index}"
      >{{item}} </span>
    </div>

    <div v-show="current == 0">
      <ul>
        <li>青</li>
      </ul>
    </div>

    <div v-show="current == 1">
      <ul>
        <li>红</li>
      </ul>
    </div>

    <div v-show="current == 2">
      <ul>
        <li>白</li>
      </ul>
    </div>

    <div v-show="current == 3">
      <ul>
        <li>黑</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      current:0
    }
  },
  methods:{
    handleClick(index){
      this.current = index
    }
  }
};
</script>

<style lang='less' scoped>
.tabs {
  margin-bottom: 20px;
  span {
    cursor: pointer;   // css属性光标  // 一只手
  }
}
.active{
  color:red
}
</style>