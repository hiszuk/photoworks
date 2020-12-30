<template>
  <div>
    <page-header-large
      bgimage="/images/img-01.jpg"
      title="PHOTO WORKS"
      subtitle="Satoshi Kato"
      description="ご覧いただきありがとうございます。心に残る写真をモットーに活動しています。"
    />

    <div id="main-content" class="section">
      <div class="container has-text-centered">
        <h1 class="title has-text-white">Photo Works</h1>
      </div>
    </div>

    <contents-middle image="/images/img-02.jpg" title="Decline[斜陽]">
      <template slot="description">
        冬の夕暮れ前のホーム。<br />陽を浴びて一斉に輝く缶達が、最後の力を振り絞っているようで、切なくなる。
      </template>
    </contents-middle>
    <contents-middle
      image="/images/img-03.jpg"
      title="Dedications[奉献]"
      isright
    >
      <template slot="description">
        古来より五穀豊穣の感謝のしるしとして、また、翌年の実りへの祈りとして日本酒を奉献している。その思いがぎっしりと詰まり息をのむような迫力の社務所の一角にて。
      </template>
    </contents-middle>
    <contents-wide image="/images/img-05.jpg" title="Gazing[まなざし]">
      <template slot="description">
        古い街並みで視線を感じた。警戒するでもなく、近づいても来ない。いかにも猫らしい猫に出逢った。
      </template>
    </contents-wide>
    <contents-middle image="/images/img-04.jpg" title="Gravity[引力]">
      <template slot="description">今にも吸い込まれそうになる瞳。 </template>
    </contents-middle>
    <contents-middle
      image="/images/img-06.jpg"
      title="A Tender Day[春の日]"
      isright
    >
      <template slot="description">桜満開の川沿いの駅にて</template>
    </contents-middle>
    <contents-middle
      image="/images/img-07.jpg"
      title="Nostalgy[いつか見た夕暮れ]"
    >
      <template slot="description">夕陽に輝くススキと吉野線</template>
    </contents-middle>
    <contents-wide
      image="/images/img-08.jpg"
      title="Colorful Railway[彩り列車]"
    >
      <template slot="description">
        四季折々の自然に豊かに彩られた奈良路を走りゆく。
      </template>
    </contents-wide>
    <contents-middle image="/images/img-09.jpg" title="Flowers[華]">
      <template slot="description">
        色とりどりの花を一輪ずつ集めて作る花飾り。互いに補い、競い合う。
      </template>
    </contents-middle>
    <contents-middle
      image="/images/img-10.jpg"
      title="Rendezvous[出逢い]"
      isright
    >
      <template slot="description">
        紅に染まる彼岸華に<br />引き寄せられる蝶との逢瀬
      </template>
    </contents-middle>
    <contents-middle
      image="/images/img-11.jpg"
      title="Starry Skies[満天の輝き]"
    >
      <template slot="description">
        夏の夜の風物詩、天の川<br />曽爾高原にて
      </template>
    </contents-middle>
    <contents-middle
      image="/images/img-13.jpg"
      title="Azure Sky[紺碧の空]"
      isright
    >
      <template slot="description">
        悠久の時間の流れを感じた<br />碧く澄んだ夏の夜空
      </template>
    </contents-middle>
    <contents-wide image="/images/img-12.jpg" title="Jewelry Box[宝石箱]">
      <template slot="description">
        白く、赤く光る幾つもの灯りが、まるで宝石箱をひっくり返したように広がる。
      </template>
    </contents-wide>
  </div>
</template>

<script>
export default {}
</script>

<style scoped lang="scss">
@import '~/assets/style';
#main-content {
  background-color: $dark;
  color: $white;
}
.container {
  display: block;
  margin-bottom: 2rem;
}
</style>
