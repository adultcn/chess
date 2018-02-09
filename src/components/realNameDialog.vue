<template>
  <div class="realName">
    <el-dialog title="实名认证"
      :visible.sync="realName"
      width="55%"
      top="0"
      @close="$emit('update:show', false)"
      class="elmSyleNew">
      <div class="realMain lh35 fc4a4a4a">
        <div class="realTitle f20 tc fc000">
          关于平台账号实名认证公告
        </div>
        <div class="realSource tc">2018-2-1 12:30 来源：弈鱼网络官网</div>
        <hr class="hr">
        <div class="f18">
          <div> 您好！根据国家有关规定，弈鱼网络游戏将从2018年2月1日开始，将实行如下调整：</div>
          <div> 1.未进行实名认证的账号，将无法在游戏内充值消费；</div>
          <div> 2.新注册用户及老用户需进行实名认证后方可正常进行游戏。</div>
          <div> 为保障您的合法权益及账号安全，请先完成账号的实名认证。实名认证将对您的账号安全、找回密码等提供帮助，希望您及</div>
          <div> 时填写真实有效的资料，以免引起不必要的损失。</div>
          <div class="tr mt100">弈鱼网络运营团队</div>
        </div>
      </div>
    </el-dialog>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        realName: false,         //实名认证弹窗
      };
    },
    props: {
        show: false
    },
    watch: {
        show () {
            this.realName = this.show;
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

