<!-- @format -->

<template>
	<section
		id="imgTextType"
		class="image__wrap"
		:class="attr"
	>
		<h2 class="blind">올빼미와 부엉이</h2>
		<div
			class="imgText__inner"
			:class="layout"
		>
			<div class="imgText__txt">
				<span>{{ titles[0].title }}</span>
				<h3>{{ titles[0].desc }}</h3>
				<p>{{ titles[0].descsub }}</p>
				<ul>
					<li
						v-for="text in texts"
						v-bind:key="text"
					>
						<a href="/">{{ text }}</a>
					</li>
				</ul>
			</div>
			<div
				class="imgText__img"
				v-for="img in imgs"
				v-bind:key="img.img"
				:class="img.img"
			>
				<a
					href="/"
					:class="img.btn"
					>{{ img.desc }}</a
				>
			</div>
		</div>
	</section>
</template>
<script>
	export default {
		props: {
			attr: String,
			layout: String,
		},
		data: function () {
			return {
				titles: [
					{
						title: "비슷하지만 서로 다른 올빼미와 부엉이",
						desc: "올빼미, 그리고 부엉이",
						descsub:
							"비슷하게 생겨서 어느 동물인지 헷갈리는 두 동물을 소개합니다.",
					},
				],
				texts: [
					"올빼미에 대하여",
					"부엉이에 대하여",
					"올빼미와 부엉이에 차이는?",
					"날카로운 발톱의 소유자, 맹금류",
					"올빼미의 목은 얼마나 돌아가나요?",
					"밤을새는 부엉이",
				],
				imgs: [
					{
						img: "img1",
						desc: "귀여운 올빼미",
						btn: "red",
					},
					{
						img: "img2",
						desc: "부엉부엉 부엉이",
						btn: "blue",
					},
				],
			};
		},
	};
</script>
<style>
	/* imgTextType */
	.imgText__inner {
		display: flex;
		justify-content: space-between;
	}

	.imgText__inner > div {
		width: 32%;
		height: 500px;
	}

	.imgText__txt span {
		font-size: 16px;
		color: #666;
		text-decoration: underline;
		text-underline-position: under;
		margin-bottom: 20px;
		display: block;
	}

	.imgText__txt h3 {
		font-size: 50px;
		font-weight: 300;
		margin-bottom: 20px;
	}

	.imgText__txt p {
		font-size: 18px;
		font-weight: 300;
		line-height: 1.5;
		color: #666;
		margin-bottom: 10px;
		word-break: keep-all;
	}

	.imgText__txt ul {
		font-size: 18px;
		font-weight: 300;
		line-height: 1.6;
	}

	.imgText__txt ul li {
		position: relative;
		padding-left: 20px;
	}

	.imgText__txt ul li a {
		color: #666;
	}
	.imgText__txt ul li a:hover {
		text-decoration: underline;
	}
	.imgText__txt ul li::before {
		content: "";
		width: 5px;
		height: 5px;
		border-radius: 50%;
		position: absolute;
		left: 5px;
		top: 9px;
		background: #666;
	}

	.imgText__img {
		border-radius: 10px;
		position: relative;
	}

	.imgText__img a {
		position: absolute;
		left: 30px;
		bottom: 30px;
		background-color: #7c2b39;
		color: #fff;
		padding: 10px 30px;
		border-radius: 30px;
		display: inline-block;
	}

	.imgText__img a.blue {
		background-color: #2b387c;
	}

	.imgText__img.img1 {
		background: url(../../assets/img/imgText_bg01.jpg) no-repeat center / cover;
	}

	.imgText__img.img2 {
		background: url(../../assets/img/imgText_bg02.jpg) no-repeat center / cover;
	}
	@media (max-width: 960px) {
		.imgText__inner {
			flex-wrap: wrap;
		}
		.imgText__txt h3 {
			font-size: 40px;
		}
		.imgText__txt p {
			margin-bottom: 60px;
		}
		.imgText__inner > div.imgText__txt {
			width: 100%;
			height: auto;
			text-align: center;
		}
		.imgText__inner > div.imgText__txt ul {
			display: none;
		}
		.imgText__inner > div.imgText__img {
			width: 49%;
		}
	}
	@media (max-width: 600px) {
		.imgText__img span {
			font-size: 14px;
			margin-bottom: 20px;
		}
		.imgText__txt h3 {
			font-size: 30px;
		}
		.imgText__txt p {
			margin-bottom: 50px;
			font-size: 16px;
		}
		.imgText__inner > div.imgText__img {
			width: 100%;
			height: 200px;
		}
		.imgText__inner > div.imgText__img.img1 {
			margin-bottom: 20px;
		}
		.imgText__img a {
			left: 20px;
			bottom: 20px;
		}
	}

	/* @media(max-width:1220px){
    #imgTextType{
        width: 100%;
        margin: 0 auto;
    }
}

@media(max-width: 768px) {
    .imgText__inner{
        display: block;
        align-items: center;
    }

    .imgText__inner>div {
        width: 96%;
    }

    .imgText__inner .imgText__img{
        margin-bottom: 30px;
        width: 100%;
    }
} */
</style>
