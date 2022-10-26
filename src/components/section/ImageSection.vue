<template>
  <section id="imageType" class="image__wrap" :class="attr">
    <h2>남극의 신사 펭귄🐧</h2>
    <p>가장 유명한 두 펭귄, 황제펭귄과 아델리펭귄을 소개합니다.</p>
    <div class="image__inner" :class="layout">
      <article class="image img1">
        <h3 class="image__title">아델리펭귄(Adélie Penguin)</h3>
        <p class="image__desc">
          아델리펭귄은 작고 귀여운 외모와 달리 성격이 나쁘기로 유명합니다.
          호기심이 많고 겁이 없어서 공격성이 높은 펭귄입니다. 아델리펭귄은 집을
          짓기위해서 다른펭귄들의 조약돌을 도둑질 하기도 한답니다.
        </p>
        <a class="image__btn" href="/" title="자세히보기">자세히 보기</a>
      </article>
      <article class="image img2">
        <h3 class="image__title">황제펭귄(Emperor penguin)</h3>
        <p class="image__desc">
          황제펭귄은 지구상에 현존하는 펭귄중 가장 큰 펭귄입니다. 까만 턱시도를
          입은 듯한 모습과 추워서 항상 차렷 자세로 있는 것 때문에 별명이 남극의
          신사로 불리운답니다.
        </p>
        <a class="image__btn black" href="/" title="자세히보기">자세히 보기</a>
      </article>
    </div>
  </section>
</template>
<script>
  export default{
    props: {
      attr : String,
      layout: String,
    },
  };
</script>

<style>
/* imageType */
.image__inner {
  display: flex;
  justify-content: space-between;
}
.image {
  width: 49%;
  height: 370px;
  color: #fff;
  padding: 200px 30px 30px 30px;
  box-sizing: border-box;
}
.image.img1 {
  background: url(../../assets/img/imageType01_01.jpg) no-repeat center;
  filter: opacity(0.8) drop-shadow(0 0 black);
}

.image.img2 {
  background: url(../../assets/img/imageType01_02.jpg) no-repeat center;
  filter: opacity(0.8) drop-shadow(0 0 black);
}
.image__title {
  font-size: 32px;
  margin-bottom: 10px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.image__desc {
  font-size: 16px;
  font-weight: 300;
  margin-bottom: 10px;
  line-height: 1.5;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}
.image__btn {
  font-size: 16px;
  color: #fff;
  background-color: #b45a30;
  padding: 10px 20px;
  display: inline-block;
}
.image__btn.black {
  background-color: #21201c;
}

@media (max-width: 960px) {
}
@media (max-width: 600px) {
  .image__inner {
    flex-direction: column;
  }
  .image {
    width: 100%;
    padding: 210px 20px 20px 20px;
  }
  .image:first-child {
    margin-bottom: 20px;
  }
  .image__title {
    font-size: 24px;
  }
}
/* @media(max-width:1220px){
    #imageType{
        width: 96%;
        margin: 0 auto;
    }
    .image__inner.container{
        min-width: auto;
        width: auto;
    }

    .image__title{
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
    }
}

@media(max-width:768px){
    .image__inner{
        flex-wrap: wrap;
        justify-content: center;
    }
    .image{
        width: 100%;
        margin-bottom: 15px;
        padding: 200px 60px 60px 60px;
    }
    .image.img2{
        margin-bottom: 0;
    }
} */
</style>
