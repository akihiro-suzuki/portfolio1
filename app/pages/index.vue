<template>
  <section class="container">
    <div class="main-picture">
      <transition>
        <img id="my-picture" src="~/assets/DSC_1476.jpg" />
      </transition>
      <div>
        <p class="title">Akihiro Suzuki Portfolio</p>
        <p class="sub-title">Software Engineer</p>
        <p class="sub-title">Jazz Drummer</p>
      </div>
    </div>
    <article>
      <div id="intro">
        <div>
          <div class="about-site">
            <p class="about-site-title">このサイトについて</p>
            <p>Akihiro Suzukiのポートフォリオサイトです。</p>
            <p>
              ソフトウェアのコンテンツを載せる予定です。
            </p>
          </div>
          <div class="card">
            <p class="card-title">What's New?</p>
            <p>2019/10/07 サイトを新規作成しました</p>
          </div>
        </div>
      </div>
    </article>
  </section>
</template>

<script>
// import Logo from '~/components/Logo.vue'

export default {
  // components: {
  //   Logo
  // }
  transition: 'page'
}
</script>

<style>
.page-enter-active,
.page-leave-active {
  transition: opacity 0.2s;
}
.page-enter,
.page-leave-active {
  opacity: 0;
}
.slide-left-enter,
.slide-right-leave-active {
  opacity: 0;
  transform: translate(30px, 0);
}
.slide-left-leave-active,
.slide-right-enter {
  opacity: 0;
  transform: translate(-30px, 0);
}

.container {
  margin: 0 auto;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.main-picture {
  position: relative;
}
.main-picture div {
  position: absolute;
  /* top50%とleft50% : これでほぼ真ん中に配置されます。しかし、これだと文字の大きさ分だけ真ん中からずれてしまいます。 */
  top: 50%;
  left: 50%;
  /* translateで文字分のズレを補正 */
  transform: translate(-50%, -50%);
  /* marginやpaddingを0にして、真ん中からずれるのを防止 */
  margin: 0px;
  padding: 0px;
  font-size: 40px;
  font-weight: bold;
  font-family: 'Courier New', Courier, monospace;
  color: white;
}
#my-picture {
  width: 100%;
}
.title {
  text-shadow: 3px 3px 3px #808080;
}
.sub-title {
  font-size: 20px;
}
#intro {
  display: flex;
  justify-content: center;
  align-items: center;
}
.about-site {
  margin-bottom: 30px;
}
.about-site-title {
  font-weight: bold;
  font-size: larger;
  color: lightgray;
}
.about-site p {
  color: darkgray;
}
.card {
  width: 400px;
  margin: 20px;
  border-radius: 5px;
  background-color: #fff;
  box-shadow: 0 3px 6px #ccc;
  padding: 10px 10px 10px 10px;
}
.card-title {
  font-weight: bold;
  font-size: larger;
  padding: 6px;
  margin-bottom: 10px;
  border-bottom: 1px solid lightgray;
}
.card p {
  font-size: 14px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  color: darkgray;
}
@media screen and (max-width: 767px) {
  .title {
    font-size: 18px;
  }
  .sub-title {
    font-size: 12px;
  }
}
</style>
