<html>
    <head>
        <title>Creaturia -CountDown-</title>
    </head>
    <body>
        <style>
        body, html {
            height: 100%;
            margin: 0;
        }

        .bgimg {
            background-color:#2c2f33;
            height: 100%;
            background-position: center;
            background-size: cover;
            position: relative;
            color:#cd5334;
            font-family: "Courier New", Courier, monospace;
            font-size: 25px;
        }

        .topleft {
            position: absolute;
            top: 0;
            left: 16px;
        }

        .bottomleft {
            position: absolute;
            bottom: 0;
            left: 16px;
        }

        .middle {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
        }

        hr {
            margin: auto;
            width: 40%;
        }
        </style>

        <div class="bgimg">
          <div class="topleft">
            <p>Creaturia</p>
          </div>
          <div class="middle">
            <h1>RELEASES ON</h1>
            <p id="clock" class="small" style="font-size:30px"></p>
          </div>
        </div>

        <script>
        var countDownDate = new Date("Jan 1, 2018 00:00:00").getTime();
        var countdownfunction = setInterval(function() {
            var now = new Date().getTime();
            var distance = countDownDate - now;
            var days = Math.floor(distance / (1000 * 60 * 60 * 24));
            var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            var seconds = Math.floor((distance % (1000 * 60)) / 1000);
            document.getElementById("clock").innerHTML = days + "d " + hours + "h "
            + minutes + "m " + seconds + "s ";
            if (distance < 0) {
                clearInterval(countdownfunction);
                document.getElementById("clock").innerHTML = "EXPIRED";
            }
        }, 1000);
        </script>
    </body>
</html>

