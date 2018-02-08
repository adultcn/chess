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
        <li>资讯公告</li>
        <li @click="introduction = true">游戏介绍</li>
        <li @click="onlineExplain = true">在线充值</li>
      </ul>
      <div class="cb"></div>
    </div>
    <!-- <el-dialog title="登录"
      :visible.sync="signIn"
      width="500px"
      top="0"
      class="elmSyleNew">
      <div class="realMain lh35 fc4a4a4a">
        <div class="bc wPer80">
          <div>用户名：</div>
          <div><el-input v-model="sign.userName" placeholder="用户名"></el-input></div>
          <div>密码：</div>
          <div><el-input type="password" v-model="sign.passWord" placeholder="密码"></el-input></div>
        </div>
        <div class="mt20 tc">
           <el-button type="primary">登录</el-button>
        </div>
      </div>
    </el-dialog> -->
    <sign-dialog :show.sync="signIn"></sign-dialog>
    <!--  <el-dialog title="注册"
      :visible.sync="registerUser"
      width="500px"
      top="0"
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
          <el-button type="primary">登录</el-button>
          <el-button type="warning">重置</el-button>
        </div>
      </div>
    </el-dialog> -->
    <register-dialog :show.sync="registerUser"></register-dialog>
    <!-- <el-dialog title="实名认证"
      :visible.sync="realName"
      width="55%"
      top="0"
      class="elmSyleNew">
      <div class="realMain lh35 fc4a4a4a">
        <div class="realTitle f20 tc fc000">
          关于平台账号实名认证公告
        </div>
        <div class="realSource tc">2018-2-1 12:30 来源：弈鱼游戏官网</div>
        <hr class="hr">
        <div class="f18">
          <div> 您好！根据国家有关规定，弈鱼游戏游戏将从2018年2月1日开始，将实行如下调整：</div>
          <div> 1.未进行实名认证的账号，将无法在游戏内充值消费；</div>
          <div> 2.新注册用户及老用户需进行实名认证后方可正常进行游戏。</div>
          <div> 为保障您的合法权益及账号安全，请先完成账号的实名认证。实名认证将对您的账号安全、找回密码等提供帮助，希望您及</div>
          <div> 时填写真实有效的资料，以免引起不必要的损失。</div>
          <div class="tr mt100">弈鱼游戏运营团队</div>
        </div>
      </div>
    </el-dialog> -->
    <real-dialog :show.sync="realName"></real-dialog>
    <!-- <el-dialog title="游戏介绍"
      :visible.sync="introduction"
      width="55%"
      top="0"
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
    </el-dialog> -->
    <introduction-dialog :show.sync="introduction"></introduction-dialog>

    <!-- <el-dialog title="在线充值"
      :visible.sync="onlineExplain"
      width="55%"
      top="0"
      class="elmSyleNew">
      <div class="lh30 fc000 f18">
        <div>
          <div>
            <img src="../assets/onlineThart.png" alt="在线充值流程图" class="w">
          </div>
          <div>
              <div class="payBorder">
                <img src="../assets/alipay.png" alt="支付宝" class="fl">
                <div class="payTxt fl ml80">
                  <div class="fb mt10">支付宝支付</div>
                  <div class="fc535353 lh24 f16">支付宝是国内领先的独立第三方支付平台，您可以使用支付宝中的余额进行支付，同事还支持国内外160多家银行的在线支付。</div>
                </div>
                <div class="fl ml100">
                  <span class="immediately bgff9c00 clearfix f26 mt30 cursor" @click="recharge = true">立即充值</span>
                </div>
                <div class="cb"></div>
              </div>
              <div class="payBorder mt20">
                <img src="../assets/bankCard.png" alt="银行卡" class="fl">
                <div class="payTxt fl ml80">
                  <div class="fb mt10">银行卡支付</div>
                  <div class="fc535353 lh24 f16">支持工商银行、农业银行、招商银行、中国银行、建设银行、交通银行、兴业银行、广大银行、华夏银行、中信银行、上海浦东发展银行等全国55家主流发卡银行的网上支付功能。</div>
                </div>
                <div class="fl ml100">
                  <span class="immediately clearfix f26 mt30 cursor" @click="recharge = true">立即充值</span>
                </div>
                <div class="cb"></div>
              </div>
          </div>
          <hr class="hr">
          <div>网络虚拟货币名称：钻石</div>
          <div>充值比例：1元=1钻石</div>
          <div>我司郑重承诺：网络虚拟货币不能兑换成人民币及任何现实中的其他国家货币，发现违法兑换的行为，我司将进行严厉打击，并上报有关部门。</div>
        </div>
      </div>
    </el-dialog> -->
    <online-dialog :show.sync="onlineExplain"></online-dialog>
    <!-- <el-dialog title="在线充值"
      :visible.sync="recharge"
      width="55%"
      top="0"
      class="elmSyleNew">
      <div class="lh30 fc000 f18">
        <div class="bc wPer80">
          <div class="fc3279ed">网络虚拟货币名称：钻石</div>
          <div class="fc3279ed">充值比例：1=1钻石</div>
          <div class="fc3279ed">游戏币名称：金币</div>
          <div class="fc3279ed">兑换比例：1钻石=10000金币</div>
          <div class="sub-title">输入充值账号:</div>
          <div class="input400">
            <el-input v-model="rechargeData.account" placeholder="输入充值账号"></el-input>
          </div>
          <div class="sub-title">确认充值账号:</div>
          <div class="input400">
            <el-input v-model="rechargeData.determination" placeholder="确认充值账号"></el-input>
          </div>
          <div class="sub-title">充值金额:</div>
          <div>
            <el-select v-model="rechargeData.money" placeholder="请选择">
              <el-option
                v-for="item in rechargeData.options"
                :key="item.value"
                :label="item.label"
                :value="item.value">
              </el-option>
            </el-select>
            <div>(温馨提示：适度游戏益脑，合理安排时间，享受健康生活)</div>
          </div>
          <div class="sub-title">QQ号:</div>
          <div class="w400">
            <div class="el-select input300"><el-input v-model="rechargeData.qqNumber" placeholder="QQ号"></el-input></div>
            <span>(选填)</span>
            <div>(填写真实QQ方面掉单查询)</div>
          </div>
          <div class="fcff0000">
            *我司郑重承诺：网络虚拟货币不能兑换成人民币以及任何现实中的其他国家货币，发现违法兑换的行为，我司将进行严厉打击，并将上报有关部门。
          </div>
          <div class="tc mt10">
            <el-button type="primary">提交</el-button>
          </div>
        </div>
      </div>
    </el-dialog> -->
  </div>
</template>

<script>
  import signDialog from '@/components/signDialog'
  import registerDialog from '@/components/registerDialog'
  import realDialog from '@/components/realNameDialog'
  import introductionDialog from '@/components/introductionDialog'
  import onlineDialog from '@/components/onlineDialog'

  export default {
    data() {
      return {
        signIn: false,           //登录弹窗
        // sign: {
        //   userName: '',       //用户名
        //   passWord: ''        //密码
        // },
        registerUser: false,     //注册弹窗
        // register: {
        //   userName:'',        //用户名
        //   nickName:'',        //昵称
        //   passWord:'',        //密码
        //   passWordConfirm:'', //确认密码
        //   realName:'',        //真实姓名
        //   idNumber:'',        //身份证号
        //   phoneNumber:'',     //手机号码
        //   userService:false   //用户条框
        // },
        realName: false,         //实名认证弹窗
        introduction: false,     //游戏介绍弹窗
        // recharge: false,         //在线充值弹窗
        onlineExplain: false,    //在线充值弹窗说明
        // rechargeData:{           //在线充值值
        //   account:'',         //在线充值帐号
        //   determination:'',   //在线充值确认帐号
        //   options: [{         //在线充值充值金额下拉
        //     value: '10',
        //     label: '10元'
        //   }, {
        //     value: '30',
        //     label: '30元'
        //   }, {
        //     value: '50',
        //     label: '50元'
        //   }, {
        //     value: '100',
        //     label: '100元'
        //   }, {
        //     value: '500',
        //     label: '500元'
        //   }],
        //   money:'10',        //在线充值充值金额
        //   qqNumber:''        //在线充值QQ号
        // },
      };
    },
    components: {
        signDialog,              //登录组件
        registerDialog,          //注册组件
        realDialog,              //实名组件
        introductionDialog,      //游戏介组件
        onlineDialog,            //在线充值组件
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
