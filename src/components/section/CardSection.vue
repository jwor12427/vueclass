<template>
  <section id="cardType" class="card__wrap nexon section content__item">
    <h2>당신에게 친숙한 새들의 이야기</h2>
    <p>
      많은 이들과 함께하는 새, 까마귀, 까치, 비둘기에 대한 이야기를 풀어보아요🕊️
    </p>
    <div class="card__inner container">
      <article class="card">
        <figure class="card__header">
          <img src="../../assets/img/card_bg01_01.jpg" alt="해바라기" />
        </figure>
        <div class="card__body">
          <h3 class="tit">까마귀(Crow)</h3>
          <p class="desc">
            까마귀는 조류 중에서도 까치, 앵무새와 함께 높은 지능을 가지고 있는
            새입니다. 별다른 훈련없이 거울 속 자신을 알아보는 조류입니다.
            까마귀는 종종 도구를 사용하는 모습을 보이기도 합니다.
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="66"
                height="9"
                viewBox="0 0 66 9"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M65.3504 4.79795C65.5457 4.60269 65.5457 4.28611 65.3504 4.09084L62.1685 0.908863C61.9732 0.713601 61.6566 0.713601 61.4614 0.908863C61.2661 1.10413 61.2661 1.42071 61.4614 1.61597L64.2898 4.4444L61.4614 7.27282C61.2661 7.46809 61.2661 7.78467 61.4614 7.97993C61.6566 8.17519 61.9732 8.17519 62.1685 7.97993L65.3504 4.79795ZM0.996887 4.9444H64.9969V3.9444H0.996887V4.9444Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img src="../../assets/img/card_bg01_02.jpg" alt="별이 빛나는 밤" />
        </figure>
        <div class="card__body">
          <h3 class="tit">까치(Oriental Magpie)</h3>
          <p class="desc">
            적응력이 강한 까치는 사람이 사는 도시에서도 잘 살아가는 새입니다.
            까치의 가장 돋보이는 특징은 긴 꼬리입니다. 까치의 앉은 모습을 보면
            꽁치를 위아래로 까딱거리는 모습을 볼 수 있습니다.
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="66"
                height="9"
                viewBox="0 0 66 9"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M65.3504 4.79795C65.5457 4.60269 65.5457 4.28611 65.3504 4.09084L62.1685 0.908863C61.9732 0.713601 61.6566 0.713601 61.4614 0.908863C61.2661 1.10413 61.2661 1.42071 61.4614 1.61597L64.2898 4.4444L61.4614 7.27282C61.2661 7.46809 61.2661 7.78467 61.4614 7.97993C61.6566 8.17519 61.9732 8.17519 62.1685 7.97993L65.3504 4.79795ZM0.996887 4.9444H64.9969V3.9444H0.996887V4.9444Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img src="../../assets/img/card_bg01_03.jpg" alt="자화상" />
        </figure>
        <div class="card__body">
          <h3 class="tit">비둘기(Rock dove)</h3>
          <p class="desc">
            전세계 대도시에서 흔하게 볼수 있는 비둘기는 수명이 10년~ 20년으로 꽤
            긴편에 속합니다. 주로 단체 생활을 하며 위협을 느낄 때는 특유의
            '구르르'소리를 통해 의사를 전달합니다.
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="66"
                height="9"
                viewBox="0 0 66 9"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M65.3504 4.79795C65.5457 4.60269 65.5457 4.28611 65.3504 4.09084L62.1685 0.908863C61.9732 0.713601 61.6566 0.713601 61.4614 0.908863C61.2661 1.10413 61.2661 1.42071 61.4614 1.61597L64.2898 4.4444L61.4614 7.27282C61.2661 7.46809 61.2661 7.78467 61.4614 7.97993C61.6566 8.17519 61.9732 8.17519 62.1685 7.97993L65.3504 4.79795ZM0.996887 4.9444H64.9969V3.9444H0.996887V4.9444Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
    </div>
  </section>
</template>
<style>
/* cardType */
.card__inner {
  display: flex;
  justify-content: space-around;
}

.card {
  width: 32%;
  background-color: #f5f5f5;
}

.card__body {
  padding: 24px;
  margin-bottom: 10px;
}

.card__body .tit {
  font-size: 24px;
  margin-bottom: 10px;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.card__body .desc {
  font-size: 18px;
  line-height: 1.4;
  color: #666;
  margin-bottom: 20px;
  font-weight: 300;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
}
@media (max-width: 960px) {
  .card__inner {
    flex-wrap: wrap;
  }
  .card {
    width: 49%;
  }
  .card:last-child {
    display: none;
  }
}
@media (max-width: 600px) {
  .card {
    width: 100%;
  }
  .card:first-child {
    margin-bottom: 20px;
  }
  .card__body {
    padding: 20px;
  }
  .card__body .desc {
    font-size: 16px;
  }
}

/* @media(max-width: 1190px){
    #cardType {
        box-sizing: border-box;
        padding: 120px 20px;
    }
    .card__inner {
        display: block;
        margin: 0 auto;
    }
    .card {
        width: 100%;
        margin-bottom: 20px;
    }
    .card__body .tit {
        font-size: 20px;
    }
    .card__body .desc {
        font-size: 16px;
    }
} */
</style>
