<template>
  <div class="roll bc mt100">
    <div class="verticalBody">
      <div class="rollBody" :style="{ marginLeft: -left + 'px' }">
        <img :src="item" v-for="(item, index) in roll.img" :key="index" :class="{ active: index == sub }">
      </div>
    </div>

  </div>
</template>

<script>
  export default{
    name:'roll',
    data () {
      return{
        sub: 1,
        left: 0
      }
    },
    props:['roll'],
    created() {
      this.rollList()
    },
    methods: {
      rollList(){
        let data = this.roll;
        let len = data.img.length;

        var countDown = setInterval(() => {
          if(this.sub == (len - 1)){
            this.sub = 0;
            this.left = this.sub * 331;
          }else{
            if(this.sub != (len - 2)){
              this.left = this.sub * 331;
            }
            this.sub++;
          }
        },data.time)
      }
    }
  }
</script>

<style scoped>
  .roll{
    width: 1054px;
    height: 545px;
    overflow: hidden;
    display: table;
  }
  .verticalBody{
    text-align: center;
    vertical-align: middle;
    display: table-cell;
  }
  .rollBody{
    width: 130%;
    transition: all .6s linear;
    -webkit-transition: all .6s linear;
    -moz-transition: all .6s linear;
  }
  .roll img{
    width: 251px;
    height: 334px;
    margin-right: 40px;
    margin-left: 40px;
    transition: all .6s linear;
    -webkit-transition: all .6s linear;
    -moz-transition: all .6s linear;
  }
  .roll img.active{
    transform: scale(1.3);
    -webkit-transform: scale(1.3);
    -moz-transform: scale(1.3);
    -ms-transform: scale(1.3);
  }
</style>
