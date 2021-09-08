<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>双色球号码</title>
    <style>
        body {
            background-color: #fefefe;
        }
        
        .w {
            position: absolute;
            width: 100%;
            height: 100%;
        }
        
        .w img {
            position: relative;
            display: flex;
            margin: auto;
        }
        
        .w h1 {
            text-align: center;
        }
    </style>


</head>

<body>

    <div class="w" id="sc">
        <img src="img/seq.jpg" alt="">
        <h1>随机生成双色球号码</h1>
    </div>


    <script>
        var btn = document.getElementById('sc')
        btn.onclick = function cai1() {


            function hong1() {
                return Math.floor(Math.random() * (33 - 1 + 1)) + 1;
            }
            var hong3 = [];
            for (var i = 0; i < 6; i++) {
                hong3[i] = hong1();
            }
            // 生成初代6号码
            var hong2 = [];
            for (var q = 0; q < hong3.length; q++) {
                if (hong2.indexOf(hong3[q]) === -1) {
                    hong2.push(hong3[q]);
                }

            }

            if (hong2.length < 6) {
                var hong5 = Math.floor(Math.random() * (33 - 1 + 1)) + 1;
                for (var p = 0; p <= 6 - hong2.length; p++) {
                    hong2.push(hong5);
                }
            }

            for (var q = 0; q < hong3.length; q++) {
                if (hong2.indexOf(hong3[q]) === -1) {
                    hong2.push(hong3[q]);
                }

            }

            if (hong2.length < 6) {
                var hong5 = Math.floor(Math.random() * (33 - 1 + 1)) + 1;
                for (var p = 0; p <= 6 - hong2.length; p++) {
                    hong2.push(hong5);
                }
            }

            for (var q = 0; q < hong3.length; q++) {
                if (hong2.indexOf(hong3[q]) === -1) {
                    hong2.push(hong3[q]);
                }

            }

            if (hong2.length < 6) {
                var hong5 = Math.floor(Math.random() * (33 - 1 + 1)) + 1;
                for (var p = 0; p <= 6 - hong2.length; p++) {
                    hong2.push(hong5);
                }
            }

            // 去重补号

            for (var b = 0; b <= hong2.length - 1; b++) {
                for (j = 0; j <= hong2.length - b - 1; j++) {
                    if (hong2[j] > hong2[j + 1]) {
                        var temp = hong2[j];
                        hong2[j] = hong2[j + 1];
                        hong2[j + 1] = temp;
                    }
                }
            }

            // 排序

            function lan() {

                return Math.floor(Math.random() * (16 - 1 + 1)) + 1;
            }
            // 生成篮球
            alert('红球为' + hong2.join('-') + '蓝球为' + lan());
            // 生成
        }
    </script>

</body>

</html>


# -js-
可以随机机选双色球1.0
