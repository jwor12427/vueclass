<!-- @format -->

<template>
	<section
		id="sliderType"
		class="slider__wrap"
	>
		<swiper
			:spaceBetween="30"
			:centeredSlides="true"
			:autoplay="{
				delay: 2500,
				disableOnInteraction: false,
			}"
			:pagination="{
				clickable: true,
			}"
			:navigation="true"
			:modules="modules"
			class="mySwiper"
		>
			<swiper-slide
				v-for="title in titles"
				v-bind:key="title.title"
				:class="title.title"
			>
				<div className="desc">
					<span>{{ title.subTitle }}</span>
					<h3>{{ title.title }}</h3>
					<p>
						{{ title.desc }}<br />
						{{ title.desc2 }}
					</p>
					<div className="btn">
						<a href="/">자세히 보기</a>
						<a
							href="/"
							className="black"
						>
							사이트 보기
						</a>
					</div>
				</div>
			</swiper-slide>
		</swiper>
	</section>
</template>
<script>
	import { Swiper, SwiperSlide } from "swiper/vue";
	import "swiper/css";
	import "swiper/css/pagination";
	import "swiper/css/navigation";
	import { Autoplay, Pagination, Navigation } from "swiper";
	export default {
		components: {
			Swiper,
			SwiperSlide,
		},
		setup() {
			return {
				modules: [Autoplay, Pagination, Navigation],
			};
		},
		data: function () {
			return {
				titles: [
					{
						subTitle: "birds",
						title: "For the Birds",
						desc: "지금부터 당신에게 들려드릴 조금은 특별한",
						desc2: "새들에 대한 이야기 입니다.",
					},
					{
						subTitle: "birds",
						title: "For the Birds",
						desc: "지금부터 당신에게 들려드릴 조금은 특별한 새들에 대한 이야기 입니다.",
						desc2: "새들에 대한 이야기 입니다.",
					},
					{
						subTitle: "birds",
						title: "For the Birds",
						desc: "지금부터 당신에게 들려드릴 조금은 특별한 새들에 대한 이야기 입니다.",
						desc2: "새들에 대한 이야기 입니다.",
					},
				],
			};
		},
	};
</script>
<style>
	.slider__wrap {
		margin-top: 70px;
	}
	/* swiper */
	.swiper-slide {
		background: url(../../assets/img/SLIDER-TYPE01.jpg) no-repeat center / cover;
	}
	.swiper-slide:nth-child(2) {
		background: url(../../assets/img/SLIDER-TYPE02.jpg) no-repeat center / cover;
	}
	.swiper-slide:nth-child(3) {
		background: url(../../assets/img/SLIDER-TYPE03.jpg) no-repeat center / cover;
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
		margin-left: 10px;
	}
	.swiper-button-next,
	.swiper-button-prev {
		width: 30px !important;
		height: 56px !important;
		color: #000;
		background-image: url(../../assets/img/slider_icon.svg);
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
		background-image: url(../../assets/img/slider_icon.svg) !important;
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
		background-image: url(../../assets/img/slider_icon.svg);
		background-position: -60px -70px;
		width: 16px;
		height: 16px;
	}
	.swiper-button-play {
		background-image: url(../../assets/img/slider_icon.svg);
		background-position: -40px -70px;
		width: 16px;
		height: 16px;
	}
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
