# -7-15-<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="shortcut icon" href="./favicon.ico">
    <title>7.15</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            text-decoration: none;
            vertical-align: middle;
            list-style: none;
        }

        .banner {

            width: 100%;
            height: 390px;
            overflow: hidden;
            position: relative;
        }

        .banner-con {
            width: 11520px;
            height: 100%;
            /* margin-left: -0px; */
            transition: all .5s ease-out;
        }

        .banner a {
            display: block;
            width: 1920px;
            height: 390px;
            float: left;
            overflow: hidden;
        }

        .banner a:nth-child(1) {
            background: url(http://www.sxuek.com/statics/images/uek/banner-hyhj.jpg) center center no-repeat;
        }

        .banner a:nth-child(2) {
            background: url(http://www.sxuek.com/statics/images/uek/banner-xtyr.jpg) center center no-repeat;
        }

        .banner a:nth-child(3) {
            background: url(http://www.sxuek.com/statics/images/uek/banner00.jpg) center center no-repeat;
        }

        .banner a:nth-child(4) {
            background: url(http://www.sxuek.com/statics/images/uek/banner2.jpg) center center no-repeat;
        }

        .banner a:nth-child(5) {
            background: url(http://www.sxuek.com/statics/images/uek/banner3.jpg) center center no-repeat;
        }

        .banner a:nth-child(6) {
            background: url(http://www.sxuek.com/statics/images/uek/banner4.jpg) center center no-repeat;
        }

        .banner-bar {
            width: 420px;
            height: 20px;
            position: absolute;
            bottom: 11px;
            left: 750px;
        }

        .banner-bar li {
            width: 60px;
            height: 10px;
            margin-right: 10px;
            background-color: rgba(255, 255, 255, 1);
            float: left;
            cursor: pointer;
        }
    </style>
</head>

<body>
    <div class="banner">
        <div class="banner-con" style="margin-left: 0px;">
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
        </div>
        <ul class="banner-bar">
            <li style="background-color: rgb(38, 145, 253);"></li>
            <li style=""></li>
            <li style=""></li>
            <li style=""></li>
            <li style=""></li>
            <li style=""></li>
        </ul>
    </div>
    <script>
        var imgContainer = document.querySelector('.banner-con');
        var btns = document.querySelectorAll('.banner-bar li');
        var num = 0;
        setInterval(function () {
            for (var i = 0; i < btns.length; i++) {
                btns[i].style.backgroundColor = "";
                imgContainer.style.marginLeft = 0 + "px";
            }
            btns[num].style.background = "#2691fd";

            imgContainer.style.marginLeft = '-' + num * 1920 + "px";
            if (num == btns.length) {
                num = 0;
            } else {
                num++;
            }
        }, 1000);

        for (let i = 0; i < btns.length; i++) {
            btns[i].onclick = function () {
                num = i;
                for (let j = 0; j < btns.length; j++) {
                    btns[j].style.backgroundColor = '';
                    imgContainer.style.marginLeft = 0 + "px";
                }
                btns[i].style.background = "#2691fd";
                imgContainer.style.marginLeft = '-' + (num * 1920) + 'px';
                console.log(imgContainer.style.marginLeft);
            }
        }
    </script>

</body>

</html>
