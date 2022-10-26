<template>
  <section id="sliderType" class="slider__wrap">
    <h2 class="blind">슬라이드 영역</h2>
    <div class="slider__inner">
      <div class="slider">
        <div class="slider__img">
          <div class="desc container">
            <span>animal</span>
            <h3>animal story</h3>
            <p>
              새로추가 된 동물들의 소식을 들어보세요! <br />
              다양한 동물친구들의 이야기를 볼 수 있답니다.
            </p>
            <div class="btn">
              <a href="#">자세히 보기</a>
              <a href="#" class="black">사이트 보기</a>
            </div>
          </div>
        </div>
        <div class="slider__arrow">
          <a href="#" class="left"><span class="ir">이전 이미지</span></a>
          <a href="#" class="right"><span class="ir">다음 이미지</span></a>
        </div>
        <div class="slider__dot">
          <a href="#" class="dot active"><span class="ir">1</span></a>
          <a href="#" class="dot"><span class="ir">2</span></a>
          <a href="#" class="dot"><span class="ir">3</span></a>
          <a href="#" class="play"><span class="ir">플레이</span></a>
          <a href="#" class="stop"><span class="ir">정지</span></a>
        </div>
      </div>
    </div>
  </section>
</template>
<style>
.slider__wrap {
  margin-top: 70px;
}
.slider {
  position: relative;
}
.slider__img {
  background: url(../../assets/img/SLIDER-TYPE01.jpg) no-repeat center / cover;
}
.slider__img .desc {
  /* width: 1160px; */
  width: 90%;
  margin: 0 auto;
  padding: 100px 20px;
}
.slider__img .desc span {
  font-size: 16px;
  background-color: #fff;
  padding: 1px 14px 0 14px;
  border-radius: 30px;
  text-transform: uppercase;
  margin-bottom: 10px;
  display: inline-block;
}
.slider__img .desc h3 {
  font-size: 110px;
  font-weight: 300;
  line-height: 1;
  color: #fff;
  text-transform: uppercase;
  margin-bottom: 16px;
  margin-left: -8px;
}
.slider__img .desc p {
  font-size: 20px;
  font-weight: 300;
  color: #fff;
  line-height: 1.35;
  margin-bottom: 130px;
}
.slider__img .desc .btn a {
  font-size: 16px;
  background-color: #fff;
  padding: 11px 50px;
  display: inline-block;
}
.slider__img .desc .btn a.black {
  background: rgb(87, 87, 87);
  color: #fff;
}
.slider__arrow a {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: 30px;
  height: 56px;
  background-image: url(../../assets/img/slider_icon.svg);
}
.slider__arrow a.left {
  left: 20px;
}
.slider__arrow a.right {
  right: 20px;
  background-position: -50px 0;
}
.slider__dot {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  bottom: 25px;
}
.slider__dot a {
  display: inline-block;
  width: 16px;
  height: 16px;
  background-image: url(../../assets/img/slider_icon.svg);
  background-position: -20px -70px;
}
.slider__dot a.active {
  background-position: 0 -70px;
}
.slider__dot a.play {
  background-position: -40px -70px;
}
.slider__dot a.stop {
  background-position: -60px -70px;
}
/* swiper */
/* .swiper-slide {
  background: url(../img/SLIDER-TYPE01.jpg) no-repeat center / cover;
}
.swiper-slide:nth-child(2) {
  background: url(../img/SLIDER-TYPE02.jpg) no-repeat center / cover;
}
.swiper-slide:nth-child(3) {
  background: url(../img/SLIDER-TYPE03.jpg) no-repeat center / cover;
}
.swiper-slide .desc {
  width: 1160px;
  margin: 0 auto;
  padding: 100px 20px;
  box-sizing: border-box;
}
.swiper-slide .desc span {
  font-size: 16px;
  background-color: #fff;
  padding: 1px 14px 0 14px;
  border-radius: 30px;
  text-transform: uppercase;
  margin-bottom: 10px;
  display: inline-block;
}
.swiper-slide .desc h3 {
  font-size: 110px;
  font-weight: 300;
  line-height: 1;
  color: #fff;
  text-transform: uppercase;
  margin-bottom: 16px;
  margin-left: -8px;
}
.swiper-slide .desc p {
  font-size: 20px;
  font-weight: 300;
  color: #fff;
  line-height: 1.35;
  margin-bottom: 130px;
}
.swiper-slide .desc .btn a {
  font-size: 16px;
  background-color: #fff;
  padding: 11px 50px;
  display: inline-block;
}
.swiper-slide .desc .btn a.black {
  background: rgb(105, 105, 105);
  color: #fff;
}
.swiper-button-next,
.swiper-button-prev {
  width: 30px !important;
  height: 56px !important;
  color: #000;
  background-image: url(../img/slider_icon.svg);
}
.swiper-button-next {
  background-position: -50px 0;
}
.swiper-button-next::after,
.swiper-button-prev::after {
  opacity: 0;
}
.swiper-pagination-bullet {
  width: 16px !important;
  height: 16px !important;
  background-image: url(../img/slider_icon.svg) !important;
  background-position: -20px -70px !important;
  background-color: transparent !important;
  opacity: 1 !important;
}
.swiper-pagination-bullet-active {
  background-position: 0px -70px !important;
}
.swiper-button {
  position: absolute;
  left: 50%;
  margin-left: 40px;
  bottom: 24px;
  z-index: 1000;
  display: flex;
  cursor: pointer;
}
.swiper-button-stop {
  background-image: url(../img/slider_icon.svg);
  background-position: -60px -70px;
  width: 16px;
  height: 16px;
}
.swiper-button-play {
  background-image: url(../img/slider_icon.svg);
  background-position: -40px -70px;
  width: 16px;
  height: 16px;
} */
@media (max-width: 960px) {
  .swiper-slide .desc {
    width: 100%;
    text-align: center;
  }
  .swiper-slide .desc h3 {
    font-size: 70px;
  }
}
@media (max-width: 600px) {
  .swiper-slide .desc {
    padding: 80px 0;
  }
  .swiper-slide .desc h3 {
    font-size: 40px;
  }
  .swiper-slide .desc p {
    font-size: 16px;
    margin-bottom: 50px;
  }
  .swiper-slide .desc .btn a {
    padding: 10px 25px;
  }
}

/* @media(max-width : 1190px) {
    .slider__inner {
        width: 100%;
        box-sizing: border-box;
    }
    .slider__img {
        width: 100%;
    }
    .slider__img .desc {
        margin: 0 auto;
    }
    .slider__img .desc span {
        font-size: 16px;
        background-color: #fff;
        padding: 1px 14px 0 14px;
        border-radius: 30px;
        text-transform: uppercase;
        margin-bottom: 10px;
        display: inline-block;
    }
    .slider__img .desc h3 {
        font-size: 9vw;
        font-weight: 300;
        line-height: 1;
        color: #fff;
        text-transform: uppercase;
        margin-bottom: 16px;
        margin-left: -8px;
    }
    .slider__img .desc p {
        font-size: 4vw;
        font-weight: 300;
        color: #fff;
        line-height: 1.35;
        margin-bottom: 130px;
    }
    .slider__arrow a {
        display: none;
    }
} */
</style>
