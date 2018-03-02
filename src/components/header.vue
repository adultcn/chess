<template>
  <div class="header f20">
    <div class="headerMain">
      <div class="fc7696c9 fl login">
        <span class="cursor" @click="signIn = true">登录</span>
        <span class="ml15 mr15">|</span>
        <span class="cursor" @click="registerUser = true">注册</span>
      </div>
      <ul class="fc fcwhite fl">
        <li @click="realName = true">实名认证</li>
        <li @click="information = true">资讯公告</li>
        <li @click="introduction = true">游戏介绍</li>
        <li @click="onlineExplain = true">在线充值</li>
        <li @click="wardship = true">家长监护</li>
      </ul>
      <div class="cb"></div>
    </div>

    <sign-dialog :show.sync="signIn"></sign-dialog>
    <register-dialog :show.sync="registerUser"></register-dialog>
    <real-dialog :show.sync="realName"></real-dialog>
    <introduction-dialog :show.sync="introduction"></introduction-dialog>
    <online-dialog :show.sync="onlineExplain"></online-dialog>
    <wardship-dialog :show.sync="wardship"></wardship-dialog>
    <information-dialog :show.sync="information"></information-dialog>
  </div>
</template>

<script>
  import signDialog from '@/components/signDialog'
  import registerDialog from '@/components/registerDialog'
  import realDialog from '@/components/realNameDialog'
  import introductionDialog from '@/components/introductionDialog'
  import onlineDialog from '@/components/onlineDialog'
  import wardshipDialog from '@/components/wardshipDialog'
  import informationDialog from '@/components/informationDialog'

  export default {
    data() {
      return {
        signIn: false,           //登录弹窗
        registerUser: false,     //注册弹窗
        realName: false,         //实名认证弹窗
        introduction: false,     //游戏介绍弹窗
        onlineExplain: false,    //在线充值弹窗说明
        wardship: false,         //家长监护
        information: false,      //资讯
      };
    },
    components: {
        signDialog,              //登录组件
        registerDialog,          //注册组件
        realDialog,              //实名组件
        introductionDialog,      //游戏介组件
        onlineDialog,            //在线充值组件
        wardshipDialog,          //家长监护
        informationDialog,       //资讯
    },
    methods: {
      open() {
        const h = this.$createElement;
        this.$msgbox({
          message: '<img src="' + require('../assets/crab.png') + '" class="mt50">',
          dangerouslyUseHTMLString: true,
          center:true,
          customClass:'construction',
          showCancelButton: false,
        });
      }
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .elmSyleNew .payBorder{
    padding: 20px 10px;
    border:2px solid #ababab;
  }
  .elmSyleNew .payBorder .payTxt{
    width:320px
  }

  .headerMain{
    height: 77px;
    line-height: 77px;
    background: #1d2d48;
  }
  .header .login{
    margin-left: 20%;
  }
  .header ul{
    margin-left: 20%;
  }
  .header ul li{
    width:1.1rem;
    text-align: center;
    float: left;
    cursor: pointer;
  }
</style>
