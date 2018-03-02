<template>
  <div class="introduction">
    <el-dialog title="游戏介绍"
      :visible.sync="introduction"
      width="55%"
      top="0"
      @close="$emit('update:show', false)"
      class="elmSyleNew">
      <div class="lh35 fc000 f18 h500 overflow_y">
        <div class="fc3279ed">游戏介绍</div>
        <div>最经典的欢乐捕鱼，这里有最炫酷的炮台星宿炮台、剃刀炮台；最绚丽的海底世界，鱼种丰富，龙王娜迦等你来打。玩家需要消耗炮弹来捕获鱼类，就能获得对应的金币奖励。炮弹威力（100-10000）×捕获鱼类的倍数。</div>
        <div class="fc3279ed mt20">游戏预览</div>
        <div>
          <img src="../assets/introduction1.png" alt="游戏预览" class="fl">
          <img src="../assets/introduction2.png" alt="游戏预览" class="ml30">
        </div>
        <div class="fc3279ed mt20">基本规则</div>
        <div>房间设定：四个房间，初级福利场新手玩家最强福利，中级场、高级场更有强力BOSS，至尊VIP场等你来战！</div>
        <div class="fc3279ed mt20">操作规则</div>
        <div>点击屏幕发射子弹，玩家炮台左右侧按钮为加减炮，屏幕左侧按钮为锁定/解除。</div>
        <div class="fc3279ed mt20">鱼类规则</div>
        <div>小黄鱼（2倍）：因其外形酷似小蝌蚪而得其名，常成群结队，容易打击，常一网多鱼</div>
        <div>扯旗鱼（2倍）：通体红色，极易捕捉。 </div>
        <div>蓝色金枪鱼（3倍）：通体蓝色的金枪鱼，游动速度非常快。</div>
        <div>红杉鱼（5倍）：有着像斑马一样的条纹，打击难度不大。</div>
        <div>大头鱼（4倍）：有着两只像极了昆虫的眼睛，显得比较萌。</div>
        <div>橙灯笼鱼（5倍）：顶着发光的触须，身穿浅蓝色耀眼鱼身，犹如茫茫海底一盏明亮的引航灯，常穿插在鱼群之间。</div>
        <div>神仙鱼（6倍）：和斑马鱼一样也有着炫目的条纹，不同的地方在于它有着尖尖的嘴巴。</div>
        <div>小丑鱼（8倍）：橙白相间，扁平，打击难度不算太打。</div>
        <div>海星（10倍）：金黄的肤色加上如刺猬般的尖刺，让人印象深刻。</div>
        <div>石头鱼（8倍）：通体深蓝色的海之精灵。</div>
        <div>虎鱼（10倍）：顶着发光的触须，身穿浅蓝色耀眼鱼身，犹如茫茫海底一盏明亮的引航灯，常穿插在鱼群之间。</div>
        <div>鲶鱼（12倍）：笨拙的身躯，短小的四腿，慢慢悠游行于海底，甚是可爱。千万不要因龟速而小看他们，要想收入事囊中还得要番技巧才行。</div>
        <div>鲂鱼（15倍）：全身红色，给人视觉的冲击风暴。</div>
        <div>狮子鱼（18倍）：深海中的美丽仙子，蝴蝶鱼，要打中她难度不小哦。</div>
        <div>乌贼（23倍）：游行的途中会喷出黑色液体，需要小心跟在他的身后。</div>
        <div>剑鱼（50倍）：尖锐的嘴巴，有很强的攻击性，是鲨鱼中游行速度较快的一种。</div>
        <div>蝙蝠鱼（30倍）：体型较为庞大，魔鬼般的鱼鳍，犹如黑夜的星空，防御力较强。</div>
        <div>鳄鱼（30倍）：骄傲的鳄鱼，血量极高，防御能力超强。</div>
        <div>食人鱼（66倍）：金色的外衣显示出深海霸主的气质，得下足重金集中火力强势攻击才行。</div>
        <div>海豹（70倍）：高端，大气，上档次。</div>
        <div>美人鱼（110倍）：上半身是美丽的女人，下半身是披着鳞片的鱼尾，既富有诱惑力，又便于迅速逃遁。</div>
        <div>黑鲨（90倍）：体型巨大的海龟，防御力惊人。</div>
        <div>白龙（140倍）：传说中的百鸟之王，既能上天又能如海。</div>
        <div>金甲锤头鲨（140倍）：海洋中神秘的存在，拥有极强的闪躲能力。</div>
        <div>娜迦（140倍）：海洋中神秘的存在，拥有极强的闪躲能力。</div>
        <div class="fc3279ed mt20">炮台</div>
        <div>破晓：射击倍数X1 捕鱼概率X1</div>
        <div>闪电：射击倍数X2 捕鱼概率X2</div>
        <div>星宿：射击倍数X3 捕鱼概率X3</div>
        <div>炎阳：射击倍数X4 捕鱼概率X4</div>
        <div class="fc3279ed mt20">游戏道具</div>
        <div>冰冻：使用后将会定屏10秒钟，建议在大鱼出没时使用。</div>
        <div>狂暴：使用后将会提高炮台的射击速度。</div>
        <div>威力：使用后将消耗多倍炮弹，同时增加多倍消耗。</div>
        <div>死亡追踪：使用后的20秒内，可选择单个目标锁定攻击。</div>
      </div>
    </el-dialog>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        introduction: false,     //游戏介绍弹窗
      };
    },
    props: {
        show: false
    },
    watch: {
        show () {
            this.introduction = this.show;
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

