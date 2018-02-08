<template>
  <div class="signIn">
    <el-dialog title="登录"
      :visible.sync="signIn"
      width="500px"
      top="0"
      @close="$emit('update:show', false)"
      class="elmSyleNew">
      <div class="realMain lh35 fc4a4a4a">
        <div class="bc wPer80">
          <div>用户名：</div>
          <div><el-input v-model="sign.userName" placeholder="用户名"></el-input></div>
          <div>密码：</div>
          <div><el-input type="password" v-model="sign.passWord" placeholder="密码"></el-input></div>
        </div>
        <div class="mt20 tc">
           <el-button type="primary" @click="openCrab">登录</el-button>
        </div>
      </div>
    </el-dialog>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        signIn: false,        //登录弹窗
        sign: {
          userName: '',       //用户名
          passWord: ''        //密码
        },
      };
    },
    props: {
        show: false
    },
    watch: {
        show () {
            this.signIn = this.show;
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

