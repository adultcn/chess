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
          <a href="http://game-exe.oss-cn-hangzhou.aliyuncs.com/1.0.2/%E5%A4%A9%E4%B9%90%E6%8D%95%E9%B1%BC1.0.2.zip">
            <span class="downloadPc pa cursor ti999">pc端下载</span>
          </a>
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
              皮皮欢乐捕鱼交流群<br>
              群号：557849366
            </div>
        </div>
        <div class="guardianship pa cursor" @click="wardship = true">
          <img src="../assets/guardianship.png" alt="家长监护">
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
    <!-- <el-dialog title="家长监护"
      :visible.sync="wardship"
      width="55%"
      top="0"
      class="elmSyleNew">
      <div class="lh35 fc000 f16 h500 overflow_y">
        <el-tabs>
          <el-tab-pane label="系统介绍">
            <div class="ti2em">“网络游戏未成年人家长监护工程”是一项由完美时空、盛大游戏、腾讯、网易、搜狐畅游、巨人六家网络游戏企业共同发起并参与实施，由中华人民共和国文化部指导，旨在加强家长对未成年人参与网络游戏的监护，引导未成年人健康、绿色参与网络游戏，和谐家庭关系的社会性公益行动。 “家长监护机制”是灵猴网络游戏在这一公益行动中，针对目前未成年人缺乏自控及自律能力，容易陷入沉迷；少数监护人缺少时间照顾孩子，不能及时监督孩子游戏时间的现状，而推出的一种可由家长实施监控，纠正部分未成年子女沉迷游戏的保护机制。</div>
            <div class="ti2em">监控内容： 根据监护人意愿屏蔽游戏账号的登录应用。</div>
            <div class="ti2em">申请要求：</div>
            <div class="ti2em">1.申请人应提交较完备的申请材料，对未提供的信息要及时补充；可请熟知电脑、互联网、游戏的人员进行协助，以便提供详实 资料.</div>
            <div class="ti2em">2.申请人应保证提交的信息真实有效；对于提供虚假信息或伪造证件，我司将保留进一步追究法律责任的权利。</div>
            <div class="ti2em">《未成年人健康参与网络游戏提示》 </div>
            <div class="ti2em">随着网络在青少年中的普及，未成年人接触网络游戏已经成为普遍现象。为保护未成年人健康参与游戏，在政府进一步加强行业管理的前提下，家长也应当加强监护引导。为此，我们为未成年人参与网络游戏提供以下意见：</div>
            <div class="ti2em">一、主动控制游戏时间。游戏只是学习、生活的调剂，要积极参与线下的各类活动，并让父母了解自己在网络游戏中的行为和体验。</div>
            <div class="ti2em"> 二、不参与可能耗费较多时间的游戏设置。不玩大型角色扮演类游戏，不玩有PK类设置的游戏。在校学生每周玩游戏不超过2小时，每月在游戏中的花费不超过10元。</div>
            <div class="ti2em">三、不要将游戏当作精神寄托。尤其在现实生活中遇到压力和挫折时，应多与家人朋友交流倾诉，不要只依靠游戏来缓解压力。</div>
            <div class="ti2em">四、养成积极健康的游戏心态。克服攀比、炫耀、仇恨和报复等心理，避免形成欺凌弱小、抢劫他人等不良网络行为习惯。</div>
            <div class="ti2em">五、注意保护个人信息。包括个人家庭、朋友身份信息，家庭、学校、单位地址，电话号码等，防范网络陷阱和网络犯罪。</div>
          </el-tab-pane>
          <el-tab-pane label="申请流程">
            <div class="tc">
              <img src="../assets/process.png" alt="申请流程">
            </div>
            <div class="ti2em">季度报告</div>
            <div class="ti2em">季度我公司游戏平台会在每季度末向浙江省文化行政部门提交“家长监护工程”情况报告。报告内容包括咨询数量、申请数量、受理与完成情况、重点案例分析、疑难问题说明，对于工程实施过程中出现的问题提出意见或建议。报告</div>
          </el-tab-pane>
          <el-tab-pane label="服务申请">
            <div class="ti2em">申请条件：</div>
            <div class="ti2em">1、 申请人需为被监护未成年人的法定监护人；</div>
            <div class="ti2em">2、 申请人的被监护人年龄小于18周岁；</div>
            <div class="ti2em">3、 申请人需为大陆公民，不含港、澳、台人士。</div>
            <div class="ti2em">申请需提交材料：</div>
            <div class="ti2em">1、监护人信息表（包含监护人的身份证明复印件）；</div>
            <div class="ti2em">2、被监护人信息表（包含被监护人所玩游戏相关信息及身份证明复印件）；</div>
            <div class="ti2em">3、填写网络游戏未成年人家长监护申请书、保证书、授权书并手工签字（需下载，填写并打印，签字）；</div>
            <div class="ti2em">4、申请人与被监护人的监护关系证明文件（户口簿或有关机关出具的证明文件）。</div>
            <div class="ti2em">申请方式：</div>
            <div class="ti2em">1.电话服务 监护人可以通过来专线电话来咨询。</div>
            <div class="ti2em">2.接待服务 监护人可以直接上门进行申请，接待服务受理时间为周一至周五（9:30—17:15），此外国家法定假期不在接待日内 接待地址：浙江省杭州市经济技术开发区金沙世纪大厦1803室。</div>
            <div class="ti2em">其他要求：</div>
            <div class="ti2em">1.申请人应提交较完备的申请材料，对未提供的信息要及时补充；可请熟知电脑、互联网、游戏的人员进行协助，以便提供详实资料；</div>
            <div class="ti2em">2.申请人应保证提交的信息真实有效；对于提供虚假信息或伪造证件，我司将保留进一步追究法律责任的权利。</div>
            <div class="ti2em">监护服务查询：</div>
            <div class="ti2em">如果您已经申请家长监护服务，您可以联系我们了解您所提交的服务申请最新处理进展，如：传真是否收到，是否需要后续提交信息，账号是否已经进行处理等。服务期间，如果您对需要提交的信息或者处理结果有疑问，或者其他任何问题，您均可以随时联系我们，我们将由专门负责的客服主管为您提供咨询解答服务，或者配合、指导您解决问题。</div>
          </el-tab-pane>
          <el-tab-pane label="常见问题">
            <div class="ti2em fb">Q1：我可以通过哪些渠道与弈鱼网络游戏取得联系？</div>
            <div class="ti2em">A：您可以通过邮件或来访的方式联系我们： 676576419@qq.com来访地址：浙江省杭州市经济技术开发区金沙世纪大厦1803室</div>
            <div class="ti2em fb">Q2：你们这项服务收费吗？</div>
            <div class="ti2em">A：这项服务是免费的，我们会在对您提交的信息确认无误后，尽快处理。</div>
            <div class="ti2em fb">Q3：你们的服务过程大概是什么样的？</div>
            <div class="ti2em">A：第一步：联系我们，并提交信息； 第二步：会有专业的家长监护主管回访您； 第三步：如信息确认过程中，有需要您配合补充资料的情况，我们将联系您； 第四步：资料确认无误后，会按您的需求对监护账号进行处理。</div>
            <div class="ti2em fb">Q4：弈鱼网络游戏对未成年人家长监护系统的受理时间是什么？</div>
            <div class="ti2em">A：我们的服务受理时间是： 热线、传真及网络接待服务为7*24小时。（遇法定假日服务时间另行通知） 来访接待为：周一至周五，早9：00至下午17：00</div>
            <div class="ti2em fb">Q5：我发送的信息通过什么方式提供给你们？</div>
            <div class="ti2em">A：通过传真、信件或快递的方式发送给我们即可。</div>
            <div class="ti2em fb">Q6：我要对我的被监护人申请监管，需要提供哪些信息？</div>
            <div class="ti2em">A：我们需要您提供以下信息： 1、派出所出示的监护关系证明； 2、监护人信息表； 3、被监护人信息表； 4、网络游戏未成年人家长监护服务申请表； 请注意：申请表中涉及签名的部分需要手写签名。</div>
            <div class="ti2em fb">Q7：为什么还得提交起诉保证书和授权书？</div>
            <div class="ti2em">A：起诉保证书的作用是当我们按监护人的需求，在对所提交信息审核无误后，进行控制的过程中，如有用户向我公司提出书面异议，我公司可按照监护人提供的联系地址向其发送书面通知，且监护人保证在我公司通知规定的时间内，按照我公司要求对异议人提起诉讼，以确认被申请账号的归属和使用权利。如监护人在上述期限内不对异议人提起诉讼，我公司将视为此监护人同意终止处理其申请，并由我公司自主决定是否解除对被申请帐号的控制措施，监护人没有任何异议。 授权书的作用是当我公司对被监护人账号采取控制措施或其他调查措施后，一旦有第三人对我公司的行为提出异议，在得到提起需求的申请人同意并授权后，我公司可以将提起需求申请人的真实身份资料和联系方式提供给该第三人，以方便该第三人对提供虚假信息或恶意干扰第三人游戏权利者提起诉讼。由此而引起的一切法律责任均由此申请人承担。</div>
            <div class="ti2em fb">Q8：为什么我提供的信息错误，会对第三方的利益造成损害呢？</div>
            <div class="ti2em">A：因为有些信息，如账号、角色名相似度比较高，且角色名命名时还可能有特殊符号。如果您提交的信息错误，会导致我们对账号锁定失败或锁定错误。一旦我们对账号采取了措施，会影响其他玩家的游戏利益，同时也会延误您的申请处理进度。</div>
            <div class="ti2em fb">Q9：你们不相信我是他(她)的监护人吗?</div>
            <div class="ti2em">A：为避免在处理过程中可能出现的问题，我们需要您提供与账号使用者必要的监护证明关系材料。</div>
            <div class="ti2em fb">Q10：你们表中有些信息我提供不了，我该怎么办？</div>
            <div class="ti2em">A：您可以提供一些辅助信息，如：IP地址、您被监护人登录游戏的时间点及时长、游戏角色级别、账号、角色名、游戏截图、视频等。建议您可以问一下周围熟悉的人或者朋友是否有玩游戏，请他们协助您获取一些信息，或者帮助了解一些信息，这样能够加快处理进程。</div>
            <div class="ti2em fb">Q11：你们为什么不相信这是我家人的账号呢？</div>
            <div class="ti2em">A：如果申请人提交资料中的申请人或被监护人的身份证号码与被监控账户注册信息中的身份证号码一致，我们将按与您协商的结果对被监控账号立刻进行处理；如申请人提交的资料中的申请人或被监护人的身份证号码与被监控账户注册信息中的身份证号码无任何关联，为保障申请人的需求能够得到处理，以及账号使用人的利益，我们需要申请人补充提供相关的信息，以确定真实的账号。</div>
            <div class="ti2em fb">Q12：你们让我提供这些信息都是干什么用的？</div>
            <div class="ti2em">A：为了避免给您和其他人带来一些不必要的困扰和麻烦。我们会根据这些信息对账号的归属进行验证和判定，以确保为您服务的准确性。</div>
            <div class="ti2em fb">Q13：你们可以帮我针对我被监护人的账号做哪些处理?</div>
            <div class="ti2em">A：我们会在确认您提供的信息无误后，根据您的要求提供以下处理方案： 1、将该账号纳入未成年人家长监护系统； 2、将账号与监护人手机绑定，使监护人实时获得账号游戏时间信息； 3、只限定周末2天可以进行游戏； 4、经过监护人确认每天游戏的时间； 5、对账号登录采取措施。</div>
            <div class="ti2em fb">Q14：你们为什么把我提交的信息公示在网站上？</div>
            <div class="ti2em">A：我们将监护人的账号、服务器、角色名称在网站上公示是为了告知被监护方，让其本人知晓。账号相关信息一部分以星号代替，所以请您放心信息的保密性。</div>
            <div class="ti2em fb">Q15：我怎么知道申请监护的处理进度？</div>
            <div class="ti2em">A：您可以通过监护系统页面，输入您的服务码查询处理进度。</div>
            <div class="ti2em fb">Q16：我提交信息后你们何时开始受理？</div>
            <div class="ti2em">A：我们在收到您的信息，审核后，会在收到信息的48小时之内与您取得联系，对该服务进行说明，并明确告知是否需要您的后续配合。待最终确定账号无误后，我们将对账号进行监控，同时在网站公示15天。公示期内如果没有其他客户提出异议，我们会在公示结束第二天与您协商处理方案并进行处理。</div>
            <div class="ti2em fb">Q17：为什么我想封我孩子的号那么麻烦?</div>
            <div class="ti2em">A：如果您孩子账号注册的身份证与您提供的信息一致，我们将按与您协商的结果对被监控账号立刻进行处理；若您提供的信息与账号信息不一致，为防止可能由于您提供信息错误，而影响账号实际使用者的利益我们需要进行调查，来判断账号使用者与您的关系。通过上述措施，以帮助我们找到正确的账号，保证您能对孩子真实的游戏账号进行有效的监控。</div>
          </el-tab-pane>
        </el-tabs>

      </div>
    </el-dialog> -->
    <wardship-dialog :show.sync="wardship"></wardship-dialog>
  </div>
</template>

<script>
  import rollPic from '@/components/roll'
  import wardshipDialog from '@/components/wardshipDialog'
  export default {
    name: 'home',
    data (){
      return {
        rollPic:{
          img:[require('../assets/adPic1.png'),require('../assets/adPic2.png'),require('../assets/adPic3.png'),require('../assets/adPic4.png')],
          time:4000
        },
        wardship: false
      }
    },
    components: {
        rollPic,
        wardshipDialog
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
