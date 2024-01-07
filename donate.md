<!DOCTYPE html>
<html lang="zh"><head><meta charset="utf-8">
	<title>感谢打赏</title>
	<meta name="robots" content="noindex, nofollow">
	<meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1.0, maximum-scale=1.0, minimal-ui">
<style>
html, html>body {
	margin: 0px !important;
	padding: 0px !important;
	height: 100%;
	width: 100%;
}
body {
	font-family: "Helvetica Neue", Ubuntu, "WenQuanYi Micro Hei", Helvetica, "Hiragino Sans GB", "Microsoft YaHei", "Wenquanyi Micro Hei", "WenQuanYi Micro Hei Mono", "WenQuanYi Zen Hei", "WenQuanYi Zen Hei", "Apple LiGothic Medium", "SimHei", "ST Heiti", "WenQuanYi Zen Hei Sharp", Arial, sans-serif;
	-webkit-font-smoothing:antialiased;
	line-height: 1.8em;
	text-shadow: 0 0 1px rgba(255,255,255,0.1);
	background: #fff;
}
img {border-width: 0px;}
a{
	color: #000;
	text-decoration: none;
	outline:none;
	border:none;
}
.list, .list li, .list-left li {
	list-style: none;
	list-style-type: none;
	margin: 0px;
	padding: 0px;
}
.pos-f {
	position: fixed;
}
.left-100 {
	width: 100%;
	height: 100%;
}
.blur {
	-webkit-filter: blur(3px);
	filter: blur(3px);
}
.tr3 {
	transition: all .3s;
}
#DonateText {
	position: fixed;
	font-size: 12px;
	width: 70px;
	height: 70px;
	line-height: 70px;
	color: #fff;
	background: #ffd886 url(./like.svg) no-repeat center 10px;
	background-size: 20px;
	border-radius: 35px;
	text-align: center;
	left: calc(50% - 120px);
	top: calc(50% - 60px);
	z-index: -1;
	transform: rotatez(-15deg );
}
#donateBox {
	left: calc(50% - 150px);
	top: calc(50% - 15px);
	background-color: #fff;
	border: 1px solid #ddd;
	border-radius: 6px;
	width: 299px;
	height: 28px;
	float: left;
	z-index: 1;
}
#donateBox li {
	width: 74px;
	float: left;
	text-align: center;
	border-left: 1px solid #ddd;
	background: no-repeat center center;
	background-color: rgba(204, 217, 220,0.1);
	background-size: 45px;
	transition: all .3s;
	cursor: pointer;
	overflow: hidden;
	line-height: 600px;
	height: 28px;
	-webkit-filter: grayscale(1);
	filter: grayscale(1);
	opacity: 0.5;
}
#donateBox li:hover {
	background-color: rgba(204, 217, 220,0.3);
	-webkit-filter: grayscale(0);
	filter: grayscale(0);
	opacity: 1;
}
#donateBox>li:first-child {
	border-width: 0;
}
#donateBox a {
	display: block;
}
#donateBox #PayPal {
	/**background-image: url(./qq.svg);**/
}
#donateBox>#BTC {
	background-image: url(./bitcoin.svg);
	line-height: 28px;
}
#donateBox>#BTC:hover {
	overflow: visible;
}
#BTC>button {
	opacity: 0;
	cursor: pointer;
}
#donateBox #AliPay {
	background-image: url(./alipay.svg);
}
#donateBox #WeChat {
	background-image: url(./wechat.svg);
}
#QRBox {
	top: 0;
	left: 0;
	z-index: 1;
	background-color: rgba(255,255,255,0.3);
	display: none;
    perspective: 400px;
}
#MainBox {
	cursor: pointer;
	position: absolute;
	text-align: center;
	width: 200px;
	height: 200px;
	left: calc(50% - 100px);
	top: calc(50% - 100px);
	background: #fff no-repeat center center;
	background-size: 190px;
	border-radius: 6px;
	box-shadow: 0px 2px 7px rgba(0,0,0,0.3);
    opacity: 0;
	transition: all 1s ease-in-out;
	transform-style: preserve-3d;
    transform-origin: center center;
    overflow: hidden;
}
#btc-key {
	opacity: 0;
	width: 2px;
	height: 8px;
	overflow: hidden;
	left: -2px;
	top: -8px;
}
#github {
	width: 24px;
	height: 24px;
	left: calc(50% + 135px);
	top: calc(50% - 30px);
	background: no-repeat center center url(https://acdn.moeyy.cn/jsdelivr/gh/nuoxianCN/cdn@1.0.4/pay/images/github.svg);
	background-size: contain;
	opacity: 0.3;
	transform: rotatez(15deg );
}
[data-footnote] {
	position: relative;
	overflow: hidden;
}
[data-footnote]:hover {
	overflow: visible;
}
[data-footnote]::before, [data-footnote]::after {
	position: absolute;
	transition: all .3s;
	transform: translate3d(-50%,0,0);
	opacity: 0;
	left: 37px;
	z-index: 10;
}
[data-footnote]::before {
	content: attr(data-footnote);
	border-radius: 6px;
	background-color: rgba(100,100,100,0.8);
	color: #fff;
	height: 24px;
	line-height: 24px;
	padding: 0 6px;
	font-size: 12px;
	white-space: nowrap;
	top: -24px;
	left: 37px;
}
[data-footnote]::after {
	content: '';
	border: 5px solid #333;
	border-color: rgba(100,100,100,0.8) transparent transparent transparent;
	top: 0;
	left: 37px;
}
[data-footnote]:hover::before,[data-footnote]:hover::after {
	opacity: 1;
}
[data-footnote]:hover::before,[data-footnote]:hover::after {
	transform: translate3d(-50%,-7px,0);
}

#MainBox.showQR {
	opacity: 1;
    animation-name:showQR;
    animation-duration:3s;
    animation-timing-function:ease-in-out;
    animation-iteration-count:1;
    animation-fill-mode:forwards;
    -webkit-animation:showQR 3s ease-in-out 0s 1 normal forwards;
}
@keyframes showQR {
	from {
		transform: rotateX(90deg);
	}
	8% {
		opacity: 1;
		transform: rotateX(-60deg);
	}
	18% {
		opacity: 1;
		transform: rotateX(40deg);
	}
	34% {
		opacity: 1;
		transform: rotateX(-28deg);
	}
	44% {
		opacity: 1;
		transform: rotateX(18deg);
	}
	58% {
		opacity: 1;
		transform: rotateX(-12deg);
	}
	72% {
		opacity: 1;
		transform: rotateX(9deg);
	}
	88% {
		opacity: 1;
		transform: rotateX(-5deg);
	}
	96% {
		opacity: 1;
		transform: rotateX(2deg);
	}
	to {
		opacity: 1;
	}
}
#MainBox.hideQR {
	opacity: 1;
    animation-name:hideQR;
    animation-duration:0.5s;
    animation-timing-function:ease-in-out;
    animation-iteration-count:1;
    animation-fill-mode:forwards;
    -webkit-animation:hideQR 0.5s ease-in-out 0s 1 normal forwards;
}
@keyframes hideQR {
	from {
	}
	20%,50% {
		transform: scale(1.08,1.08);
		opacity: 1;
	}
	to {
		opacity: 0;
		transform: rotateZ(40deg) scale(0.6,0.6);
	}
}
</style>

<script src="https://acdn.moeyy.cn/jsdelivr/npm/jquery@3.3.1/dist/jquery.min.js"></script>
<script src="https://acdn.moeyy.cn/jsdelivr/npm/clipboard@2.0.1/dist/clipboard.min.js"></script>

<script>
	jQuery(document).ready(function() {
	var QRBox	=	$('#QRBox');
	var MainBox	=	$('#MainBox');
	var BTCQR	=	'./no.png';
	var AliPayQR	=	'./alipay.png';
	var WeChanQR	=	'./wechat.png';
	var PayPalQR	=	"./qqpay.png";

	

	function showQR(QR) {
		if (QR) {
			MainBox.css('background-image','url('+QR+')');
		}
		$('#DonateText,#donateBox,#github').addClass('blur');
		QRBox.fadeIn(300,function(argument) {
			MainBox.addClass('showQR');
		});
	}

	$('#donateBox>li').click(function(event) {
		var thisID	=	$(this).attr('id');
		if (thisID === 'BTC') {
			showQR(BTCQR);
			new Clipboard('#BTCBn');
		} else if (thisID === 'AliPay') {
			showQR(AliPayQR);
		} else if (thisID === 'WeChat') {
			showQR(WeChanQR);
		} else if (thisID === 'PayPal') {
			//showQR(PayPalQR);
		}
	});

	MainBox.click(function(event) {
		MainBox.removeClass('showQR').addClass('hideQR');
		setTimeout (function(a) {
			QRBox.fadeOut(300,function(argument) {
				MainBox.removeClass('hideQR');
			});
			$('#DonateText,#donateBox,#github').removeClass('blur');
		},600);

	});
});
</script>
</head>

<body>
	<!-- Bitcoin 账号 -->
	<input id="btc-key" type="text" value="很遗憾~并没有BTC账号哦~" readonly="readonly">

	<div id="DonateText" class="tr3">Donate</div>
	<ul id="donateBox" class="list pos-f tr3">
		<!--li id="BTC" data-footnote="BTC不能使用，请更换其他方式赞赏！"><button id="BTCBn" data-clipboard-target="#btc-key" alt="Copy to clipboard">Bitcoin</button></li-->
		<li id="PayPal" >paypal</li>
		<li id="AliPay">AliPay</li>
		<li id="WeChat">WeChat</li>
		<li id="PayPal" >paypal</li>
	</ul>
	<div id="QRBox" class="pos-f left-100">
		<div id="MainBox"></div>
	</div>

</body></html>