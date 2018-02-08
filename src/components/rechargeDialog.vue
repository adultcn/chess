<template>
  <div class="recharge">
    <el-dialog title="在线充值"
      :visible.sync="recharge"
      width="55%"
      top="0"
      @close="$emit('update:show', false)"
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
            <el-button type="primary" @click="openCrab">提交</el-button>
          </div>
        </div>
      </div>
    </el-dialog>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        recharge: false,         //在线充值弹窗
        rechargeData:{           //在线充值值
          account:'',            //在线充值帐号
          determination:'',      //在线充值确认帐号
          options: [{            //在线充值充值金额下拉
            value: '10',
            label: '10元'
          }, {
            value: '30',
            label: '30元'
          }, {
            value: '50',
            label: '50元'
          }, {
            value: '100',
            label: '100元'
          }, {
            value: '500',
            label: '500元'
          }],
          money:'10',          //在线充值充值金额
          qqNumber:''          //在线充值QQ号
        },
      };
    },
    props: {
        show: false
    },
    watch: {
        show () {
            this.recharge = this.show;
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

