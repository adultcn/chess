<template>
  <div class="registerUser">
    <el-dialog title="注册"
      :visible.sync="registerUser"
      width="500px"
      top="0"
      @close="$emit('update:show', false)"
      class="elmSyleNew">
      <div class="realMain lh35 fc4a4a4a">
        <div class="bc wPer80">
          <div class="input280">
            <div class="w70 tr fl mr5">用户名：</div>
            <el-input v-model="register.userName" placeholder="用户名"></el-input>
          </div>
          <div class="input280 mt10">
            <div class="w70 tr fl mr5">昵称：</div>
            <el-input v-model="register.nickName" placeholder="昵称"></el-input>
          </div>
          <div class="input280 mt10">
            <div class="w70 tr fl mr5">密码：</div>
            <el-input type="password" v-model="register.passWord" placeholder="密码"></el-input>
          </div>
          <div class="input280 mt10">
            <div class="w70 tr fl mr5">确认密码：</div>
            <el-input type="password" v-model="register.passWordConfirm" placeholder="确认密码"></el-input>
          </div>
          <div class="input280 mt10">
            <div class="w70 tr fl mr5">真实姓名：</div>
            <el-input v-model="register.realName" placeholder="真实姓名"></el-input>
          </div>
          <div class="input280 mt10">
            <div class="w70 tr fl mr5">身份证号：</div>
            <el-input v-model="register.idNumber" placeholder="身份证号"></el-input>
          </div>
          <div class="input280 mt10">
            <div class="w70 tr fl mr5">手机号码：</div>
            <el-input v-model="register.phoneNumber" placeholder="手机号码"></el-input>
          </div>
          <div class="tc mt10">
              <el-checkbox v-model="register.userService">我已阅读并同意</el-checkbox><a href="../static/userservice.rar">用户服务条框</a>
          </div>
        </div>
        <div class="mt20 tc">
          <el-button type="primary" @click="openCrab">登录</el-button>
          <el-button type="warning" @click="openCrab">重置</el-button>
        </div>
      </div>
    </el-dialog>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        registerUser: false,     //注册弹窗
        register: {
          userName:'',        //用户名
          nickName:'',        //昵称
          passWord:'',        //密码
          passWordConfirm:'', //确认密码
          realName:'',        //真实姓名
          idNumber:'',        //身份证号
          phoneNumber:'',     //手机号码
          userService:false   //用户条框
        },
      };
    },
    props: {
        show: false
    },
    watch: {
        show () {
            this.registerUser = this.show;
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

