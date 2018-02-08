<template>
  <div class="introduction">
    <el-dialog title="游戏介绍"
      :visible.sync="introduction"
      width="55%"
      top="0"
      @close="$emit('update:show', false)"
      class="elmSyleNew">
      <div class="lh35 fc000 f18">
        <div class="fc3279ed">游戏介绍</div>
        <div>最经典的欢乐捕鱼，这里有最炫酷的炮台星宿炮台、剃刀炮台；最绚丽的海底世界，鱼种丰富，龙王娜迦等你来打。</div>
        <div class="fc3279ed mt80">游戏预览</div>
        <div>
          <img src="../assets/introduction1.png" alt="游戏预览" class="fl">
          <img src="../assets/introduction2.png" alt="游戏预览" class="ml30">
        </div>
        <div class="fc3279ed mt80">基本规则</div>
        <div>房间设定：四个房间，初级福利场新手玩家最强福利，中级场、高级场更有强力BOSS，至尊VIP场等你来战！</div>
      </div>
    </el-dialog>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        introduction: false,     //游戏介绍弹窗
      };
    },
    props: {
        show: false
    },
    watch: {
        show () {
            this.introduction = this.show;
        }
    },
    methods: {
      openCrab() {
        const h = this.$createElement;
        this.$msgbox({
          message: '<img src="' + require('../assets/crab.png') + '" class="mt50"><div class="f20 fcwhite">功能还在建设中</div>',
          dangerouslyUseHTMLString: true,
          center:true,
          customClass:'construction',
          showCancelButton: false,
        });
      }
    }
  };
</script>

