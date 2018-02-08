<template>
  <div class="onlineExplain">
    <el-dialog title="在线充值"
      :visible.sync="onlineExplain"
      width="55%"
      top="0"
      @close="$emit('update:show', false)"
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
                  <span class="immediately bgff9c00 clearfix f26 mt30 cursor" @click="recharge = true">立即充值</span>
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
    </el-dialog>
    <recharge-dialog :show.sync="recharge"></recharge-dialog>
  </div>
</template>

<script>
  import rechargeDialog from '@/components/rechargeDialog'

  export default {
    data() {
      return {
        recharge: false,         //在线充值弹窗
        onlineExplain: false,    //在线充值弹窗说明
      };
    },
    props: {
        show: false
    },
    watch: {
        show () {
            this.onlineExplain = this.show;
        }
    },
    components: {
        rechargeDialog,              //充值组件
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

