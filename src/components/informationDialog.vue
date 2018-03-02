<template>
  <div class="information">
    <el-dialog title="资讯公告"
      :visible.sync="information"
      width="55%"
      top="0"
      @close="$emit('update:show', false)"
      class="elmSyleNew">
     <div class="lh35 fc000 f16 h300 overflow_y">
        <el-tabs>
          <el-tab-pane label="1.0版本">
            <div class="ti2em">主要更新内容为：</div>
            <div class="ti2em">①增加全新炮台：星宿炮、阳炎炮；</div>
            <div class="ti2em">②增加实名认证奖励。</div>
            <div class="ti2em">③优化鱼阵等。</div>
            <div class="ti2em">关于游戏中的意见与建议，欢迎通过客服（QQ群号:557849366）与我们沟通。感谢您的支持与厚爱 ！</div>
          </el-tab-pane>
          <el-tab-pane label="1.1版本">
            <div class="ti2em">主要更新内容为：</div>
            <div class="ti2em">①增加全新暗黑系列BOSS，击杀即可抽取魂珠获得大量弹头；</div>
            <div class="ti2em">②优化游戏加载界面。</div>
            <div class="ti2em">关于游戏中的意见与建议，欢迎通过客服（QQ群号:557849366）与我们沟通。感谢您的支持与厚爱 ！</div>
          </el-tab-pane>
        </el-tabs>
      </div>
    </el-dialog>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        information: false,     //资讯公告弹窗
      };
    },
    props: {
        show: false
    },
    watch: {
        show () {
            this.information = this.show;
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

