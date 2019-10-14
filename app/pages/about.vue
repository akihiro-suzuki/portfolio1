<template>
  <section>
    <div class="flex-container">
      <div class="left-box">
        <img src="~/assets/about.png" />
      </div>
      <div class="right-box">
        <div>
          <p class="my-name">Akihiro Suzuki</p>
        </div>
        <div class="self-introduce">
          <p>1985年 静岡県磐田市で生まれる。</p>
          <br />
          <p>高校進学と同時に吹奏楽部に入り、打楽器を始める。</p>
          <p>
            大学でジャズ研究会と出会い、ジャズドラムを始める。
            大学院1年生時に休学し、ジャズドラマーとしての生き方を模索する。
            ジャズドラムを黒田和良氏に師事、在学中より様々なライブ活動を行う。
          </p>
          <br />
          <p>
            2010年
            神奈川県横浜市にて、システム開発会社でソフトウェアエンジニアとして勤務する。
            初期は主にAndroidアプリ開発をメインとして様々な現場を経験し、次第に様々な言語・FWを習得し、フルスタックエンジニアとしてのスキルを身に着ける。
          </p>
          <br />
          <p>
            2020年
            キャリアップのため、建設業向け自社製品・自社サービスの会社に転職する。<br />
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {}
</script>

<style scoped>
.page-enter-active,
.page-leave-active {
  transition: opacity 0.2s;
}
.page-enter,
.page-leave-active {
  opacity: 0;
}
section {
  display: flex;
  justify-content: center;
}
.flex-container {
  display: flex;
  justify-content: flex-start;
}
.left-box {
  padding: 0px 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.left-box img {
  border-radius: 30px;
}
.right-box {
  padding: 0px 20px;
}
.right-box:first-child {
  margin-bottom: auto;
}
.right-box .my-name {
  font-size: 32px;
  font-family: 'Courier New', Courier, monospace;
  color: rgb(48, 45, 45);
  padding: 0px 0px 10px 0px;
}
.self-introduce {
  width: 400px;
}
.self-introduce p {
  color: darkgray;
  font-style: italic;
  font-size: 14px;
  line-height: 2em;
  word-wrap: break-word;
}
</style>
