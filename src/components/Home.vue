<template>
  <div class="home">
    <div class="topBg tc">
      <div class="main pr bc">
        <div class="download pa">
          <div>
            <img src="../assets/pc.jpg" alt="二维码" height="138" class="code">
          </div>
          <div>
            <span class="ios clearfix pa cursor"></span>
            <span class="line clearfix pa"></span>
            <span class="android clearfix pa cursor"></span>
          </div>
        </div>
        <div>
          <!-- <a href="http://game-exe.oss-cn-hangzhou.aliyuncs.com/1.0.3/fish1.0.3.zip"> -->
            <span class="downloadPc pa cursor ti999" @click="openCrab">pc端下载</span>
          <!-- </a> -->
        </div>

        <div class="qqGroup pa">
            <div class="codeGroup lh0">
              <img src="../assets/qqGroup.png" alt="加QQ群">
              <div class="qqGroupCode">
                <img src="../assets/qqGroupCode.png" alt="加QQ群" width="130">
              </div>
              <div class="addGroup"></div>
            </div>
            <div class="f16 mt5">
              天乐捕鱼交流群<br>
              群号：557849366
            </div>
        </div>
      </div>
    </div>
    <div class="activity">
      <div class="main bc">
        <div class="tc mt50">
          <img src="../assets/activityTitle.png" alt="活动礼包">
        </div>
        <div class="package">
          <div class="packageBg packageBg1 fl"></div>
          <div class="packageBg packageBg2 fl"></div>
          <div class="packageBg packageBg3 fl"></div>
        </div>
      </div>
    </div>
    <div class="special">
      <div class="main bc">
        <div class="tc mt50 mb50">
          <img src="../assets/specialTitle.png" alt="游戏特色">
        </div>
        <div class="rollMain">
            <roll-pic :roll="rollPic"></roll-pic>
        </div>
      </div>
    </div>
    <div class="customer">
      <a target="_blank" href="http://wpa.qq.com/msgrd?v=3&amp;uin=676576419&amp;site=qq&amp;menu=yes">
        <img src="../assets/customer.png" alt="联系客服">
      </a>
    </div>
  </div>
</template>

<script>
  import rollPic from '@/components/roll'

  export default {
    name: 'home',
    data (){
      return {
        rollPic:{
          img:[require('../assets/adPic1.png'),require('../assets/adPic2.png'),require('../assets/adPic3.png'),require('../assets/adPic4.png')],
          time:4000
        }
      }
    },
    components: {
        rollPic
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
  }
</script>

<style scoped>
  .home .topBg{
    width: 100%;
    height: 7.8rem;
    background: url(../assets/top.png);
    background-size: cover;
  }
  .main{
    width: 1254px;
    height: 100%;
    overflow: hidden;
  }
  .main .guardianship{
    top: 0px;
    left: 0px;
  }
  .download{
    width: 285px;
    height: 486px;
    background: url(../assets/code.png);
    background-size: cover;
    top: 3.1rem;
  }
  .download .code {
    margin-top: 1.8rem
  }
  .download .ios{
    width: 105px;
    height: 89px;
    background: url(../assets/ios.png);
    left: 34px;
    bottom: 36px;
  }
  .download .ios:hover{
    background-position: 105px 0px;
  }
  .download .ios:active{
    background-position: 210px 0px;
  }
  .download .line{
    width: 5px;
    height: 60px;
    background: url(../assets/line.png);
    left: 136px;
    bottom: 48px;
    z-index: 1;
  }
  .download .android{
    width: 111px;
    height: 89px;
    background: url(../assets/android.png);
    right: 35px;
    bottom: 35px;
  }
  .download .android:hover{
    background-position: 111px 0px;
  }
  .download .android:active{
    background-position: 222px 0px;
  }
  .downloadPc{
    width: 457px;
    height: 130px;
    background: url(../assets/pc.png);
    left: 50%;
    bottom: 35px;
    margin-left: -228px;
  }
  .downloadPc:hover{
    background-position: 457px 0px;
  }
  .downloadPc:active{
    background-position: 914px 0px;
  }
  .qqGroup{
    width:147px;
    height: 200px;
    right: 9%;
    bottom: 17%;
  }
  .qqGroup .qqGroupCode{
    width:100%;
    height: 130px;
    background: #fff;
  }
  .qqGroup .addGroup{
    width: 100%;
    height: 35px;
    background: url(../assets/addGroup.png);
  }
  .activity{
    width: 100%;
    height: 422px;
    background: #ffc400;
  }
  .activity .packageBg{
    width: 360px;
    height: 208px;
    margin: 0 28px;
  }
  .activity .packageBg1{
    background: url(../assets/packageBg1.png);
  }
  .activity .packageBg2{
    background: url(../assets/packageBg2.png);
  }
  .activity .packageBg3{
    background: url(../assets/packageBg3.png);
  }
  .activity .packageBg:hover{
    background-position: -360px 0;
  }
  .special{
    width: 100%;
    height: 856px;
    background: url(../assets/specialBg.png)
  }
  .special .rollMain{
    width: 100%;
    height: 545px;
    background: #0c347c;
  }
  .customer{
    right: 100px;
    top: 50%;
    margin-top: -100px;
    position: fixed;
  }
</style>
