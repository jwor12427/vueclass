<!-- @format -->

<template>
	<section
		id="textType"
		class="text__wrap"
		:class="attr"
	>
		<span>{{ titles[0].desc }}</span>
		<h2 class="mb70">{{ titles[0].title }}</h2>
		<div
			class="text__inner"
			:class="layout"
		>
			<div
				class="text"
				v-for="text in texts"
				v-bind:key="text.img"
				:class="text.img"
			>
				<h3 class="text__title">{{ text.title }}</h3>
				<p class="text__desc">
					{{ text.desc }}
				</p>
				<a
					class="text_btn"
					href="/"
					>더보기</a
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
						title: "멋쟁이, 따라쟁이 앵무새🦜",
						desc: "새롭게 업데이트 된 앵무새에 종류",
					},
				],
				texts: [
					{
						img: "t1",
						title: "금강앵무",
						desc: "금강앵무는 앵무새는 대부분의 매체에서 앵무새 하면 나오는 앵무새입니다. 깃털색이 화려하며, 크기가 대형종이 속하는 앵무새 입니다.",
					},
					{
						img: "t2",
						title: "회색앵무",
						desc: "회색앵무는 앵무새중 가장 지능이 높다고 알려진 새입니다. 세계에서 가장 유명한 회색앵무는 이렌느 페퍼버그 박사의 알렉스입니다.",
					},
					{
						img: "t3",
						title: "왕관앵무",
						desc: "온순한 성격으로 길들이기 쉬워서 많은 사람들이 앵무새를 처음 접할 때 많이 추천하는 종 중 하나입니다. 겁이 많고 소심한 것이 특징입니다.",
					},
					{
						img: "t4",
						title: "코뉴어",
						desc: "가장 대중적인 앵무새이며, 애교가 많고 사람을 잘 따르는 앵무새 중 손꼽힙니다. 주로 좁은 곳이나 틈새를 파고 드는 습성이 있습니다.",
					},
					{
						img: "t5",
						title: "장미앵무",
						desc: "한국에서 많이 키우는 종류 중 하나이며, 화려한 색채 때문에 애완용으로 인기가 많습니다. 하지만 겁이 많고 예민한 성격에 자주 데리고 놀면 스트레스를 받습니다.",
					},
					{
						img: "t6",
						title: "모란앵무",
						desc: "모란앵무는 성격이 매우 활달하고 호기심이 많아 부리를 써서 탐색하는 것을 좋아합니다. 주인과 유대감이 매우 깊을 때는 주인의 옆에 꼭 붙어 있는 것이 특징입니다.",
					},
				],
			};
		},
	};
</script>
<style>
	/* textType */
	.text__inner {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
	}

	.text {
		width: 32%;
		margin-bottom: 2%;
		padding: 20px;
		box-sizing: border-box;
		border-radius: 10px;
		transition: background 0.4s;
	}

	.text:hover {
		background-color: #f5f5f5;
	}

	.text__title {
		font-size: 24px;
		line-height: 1;
		margin-bottom: 10px;
		white-space: nowrap;
		text-overflow: ellipsis;
		position: relative;
		padding-top: 75px;
	}

	.text__title::before {
		content: "";
		position: absolute;
		left: 0;
		top: 0;
		width: 60px;
		height: 60px;
		border-radius: 50%;
		background: url(../../assets/img/text_icon.svg);
	}

	.text.t1 .text__title::before {
		background-position: 0 0;
	}

	.text.t2 .text__title::before {
		background-position: -60px 0;
	}

	.text.t3 .text__title::before {
		background-position: -120px 0;
	}

	.text.t4 .text__title::before {
		background-position: -180px 0;
	}

	.text.t5 .text__title::before {
		background-position: -240px 0;
	}

	.text.t6 .text__title::before {
		background-position: -300px 0;
	}

	.text__desc {
		font-size: 18px;
		font-weight: 300;
		line-height: 1.4;
		overflow: hidden;
		text-overflow: ellipsis;
		display: -webkit-box;
		-webkit-line-clamp: 3;
		-webkit-box-orient: vertical;
		color: #666;
		margin-bottom: 20px;
	}

	.text_btn {
		font-size: 16px;
		line-height: 1;
		text-decoration: underline;
		text-underline-position: under;
		color: #666;
	}
	@media (max-width: 960px) {
		.text {
			width: 49%;
			background: #f5f5f5;
		}
	}
	@media (max-width: 600px) {
		.text__title {
			font-size: 20px;
		}
		.text__desc {
			font-size: 16px;
		}
	}
	@media (max-width: 480px) {
		.text {
			width: 100%;
		}
	}

	/* @media(max-width: 800px){
    .text__inner {
        display: block;
    }
    .text {
        width: 96%;
        margin-left: 10px;
    }
    .text__title {
        font-size: 20px;
    }
    .text__desc {
        font-size: 16px;
    }
} */
</style>
