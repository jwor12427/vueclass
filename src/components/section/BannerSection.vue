<!-- @format -->

<template>
	<section
		id="bannerType"
		class="banner__wrap"
		:class="fonts"
	>
		<h2 class="blind">배너</h2>
		<div class="banner__inner">
			<h3 class="title">{{ titles[0].title }}</h3>
			<p class="desc">
				{{ titles[0].desc }}
				<a
					:href="titles[0].link"
					:title="titles[0].alt"
					>{{ titles[0].linkdesc }}</a
				>
			</p>
			<span class="small">{{ titles[0].desc2 }}</span>
		</div>
	</section>
</template>
<script>
	export default {
		props: {
			fonts: String,
		},
		data: function () {
			return {
				titles: [
					{
						title: "새의 언어",
						desc: "더 많고, 다양한 새들의 이야기가 당신을 기다리고 있습니다.",
						link: "https://damlong.tistory.com",
						alt: "페이지 이동",
						linkdesc: "What It's Like To Be A Bird",
						desc2: "이 달의 이야기",
					},
				],
			};
		},
	};
</script>
<style>
	.banner__inner {
		background-image: url(../../assets/img/banner_bg01.jpg);
		background-repeat: no-repeat;
		background-position: center;
		text-align: center;
		padding: 120px 0;
		color: #fff;
	}
	.banner__inner .title {
		font-size: 50px;
		line-height: 1;
		font-weight: 300;
		margin-bottom: 40px;
	}
	.banner__inner .desc {
		font-size: 24px;
		line-height: 1.5;
		font-weight: 300;
		margin-bottom: 70px;
	}
	.banner__inner .desc a {
		display: block;
		color: #fff;
	}

	.banner__inner .small {
		text-decoration: underline;
	}
	@media (max-width: 960px) {
		.banner__inner {
			padding: 100px 0;
		}
	}
	@media (max-width: 600px) {
		.banner__inner {
			padding: 80px 0;
		}
		.banner__inner .title {
			font-size: 30px;
			margin-bottom: 20px;
		}
		.banner__inner .desc {
			font-size: 16px;
			margin-bottom: 40px;
		}
	}

	/* @media(max-width:1190px){
    .banner__inner{
        box-sizing: border-box;
        width: 100%;
    }
}
@media(max-width: 800px){
    .banner__inner .title {
        font-size: 30px;
    }
    .banner__inner .desc {
        font-size: 18px;
    }
} */
</style>
