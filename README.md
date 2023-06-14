
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>2048</title>

  <link href="style/main.css" rel="stylesheet" type="text/css">
  <link rel="shortcut icon" href="favicon.ico">
  <link rel="apple-touch-icon" href="meta/apple-touch-icon.png">
  <link rel="apple-touch-startup-image" href="meta/apple-touch-startup-image-640x1096.png" media="(device-width: 320px) and (device-height: 568px) and (-webkit-device-pixel-ratio: 2)"> <!-- iPhone 5+ -->
  <link rel="apple-touch-startup-image" href="meta/apple-touch-startup-image-640x920.png"  media="(device-width: 320px) and (device-height: 480px) and (-webkit-device-pixel-ratio: 2)"> <!-- iPhone, retina -->
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black">

  <meta name="HandheldFriendly" content="True">
  <meta name="MobileOptimized" content="320">
  <meta name="viewport" content="width=device-width, target-densitydpi=160dpi, initial-scale=1.0, maximum-scale=1, user-scalable=no, minimal-ui">
</head>
<body>
  <div class="container">
    <div class="heading">
      <h1 class="title">2048</h1>
      <div class="scores-container">
        <div class="score-container">0</div>
        <div class="best-container">0</div>
      </div>
    </div>
    <div id="timerbox">
        <div id="timer"> </div>
        <div class="timertile" style="color: #f9f6f2; font-size: 22px; background: #f59563">16</div>
        <div class="timertile" id="timer16" style="margin-left:6px; width:159px"></div>
        <br><br>
        <div class="timertile" style="color: #f9f6f2; font-size: 22px; background: #f67c5f">32</div>
        <div class="timertile" id="timer32" style="margin-left:6px; width:159px"></div>
        <br><br>
        <div class="timertile" style="color: #f9f6f2; font-size: 22px; background: #f65e3b">64</div>
        <div class="timertile" id="timer64" style="margin-left:6px; width:159px"></div>
        <br><br>
        <div class="timertile" style="color: #f9f6f2; font-size: 18px; background: #edcf72">128</div>
        <div class="timertile" id="timer128" style="margin-left:6px; width:159px"></div>
        <br><br>
        <div class="timertile" style="color: #f9f6f2; font-size: 18px; background: #edcc61">256</div>
        <div class="timertile" id="timer256" style="margin-left:6px; width:159px"></div>
        <br><br>
        <div class="timertile" style="color: #f9f6f2; font-size: 18px; background: #edc850">512</div>
        <div class="timertile" id="timer512" style="margin-left:6px; width:159px"></div>
        <br><br>
        <div class="timertile" style="color: #f9f6f2; font-size: 14px; background: #edc53f">1024</div>
        <div class="timertile" id="timer1024" style="margin-left:6px; width:159px"></div>
        <br><br>
        <div class="timertile" style="color: #f9f6f2; font-size: 14px; background: #edc22e">2048</div>
        <div class="timertile" id="timer2048" style="margin-left:6px; width:159px"></div>
        <br><br>
        <div class="timertile" style="color: #f9f6f2; font-size: 14px; background: #3c3a32">4096</div>
        <div class="timertile" id="timer4096" style="margin-left:6px; width:159px"></div>
        <br><br>
        <div class="timertile" style="color: #f9f6f2; font-size: 14px; background: #3c3a32">8192</div>
        <div class="timertile" id="timer8192" style="margin-left:6px; width:159px"></div>
        <br><br>
        <div class="timertile" style="color: #f9f6f2; font-size: 13px; background: #3c3a32">16384</div>
        <div class="timertile" id="timer16384" style="margin-left:6px; width:159px"></div>
        <br><br>
        <div class="timertile" style="color: #f9f6f2; font-size: 13px; background: #3c3a32">32768</div>
        <div class="timertile" id="timer32768" style="margin-left:6px; width:159px"></div>
      </div>
    <div class="above-game">
      <p class="game-intro">Join the numbers and get to the <strong>2048 tile!</strong></p>
      <a class="restart-button">New Game</a>
    </div>

    <div class="game-container">
      <div class="game-message">
        <p></p>
        <div class="lower">
	        <a class="keep-playing-button">Keep going</a>
          <a class="retry-button">Try again</a>
        </div>
      </div>

      <div class="grid-container">
        <div class="grid-row">
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
        </div>
        <div class="grid-row">
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
        </div>
        <div class="grid-row">
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
        </div>
        <div class="grid-row">
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
        </div>
      </div>

      <div class="tile-container">

      </div>
    </div>
    <p class="game-explanation"></p>
    <p class="game-explanation">
      <strong class="important">How to play:</strong><br> Use your <strong>Arrow keys, WASD keys and/or HJKL keys</strong> to move the tiles. When two tiles with the same number touch, they <strong>merge into one!</strong> Use the <strong>R key</strong> to reset.
    </p>
    <hr>
    <p>
    <strong class="important">Note:</strong> This is a modified version of 2048 built by nei on top of meep's timer mod. Original timer concept by meep can be found <a href="http:/meep.cubing.net/2048">here.</a> The game itself runs identical to the <a href="https://gabrielecirulli.github.io/2048/">original.</a>
    </p>
    <hr>
    <p>
    Created by <a href="http://gabrielecirulli.com" target="_blank">Gabriele Cirulli.</a> Based on <a href="https://itunes.apple.com/us/app/1024!/id823499224" target="_blank">1024 by Veewo Studio</a> and conceptually similar to <a href="http://asherv.com/threes/" target="_blank">Threes by Asher Vollmer.</a>
    </p>
  </div>

  <script src="js/bind_polyfill.js"></script>
  <script src="js/classlist_polyfill.js"></script>
  <script src="js/animframe_polyfill.js"></script>
  <script src="js/keyboard_input_manager.js"></script>
  <script src="js/html_actuator.js"></script>
  <script src="js/grid.js"></script>
  <script src="js/tile.js"></script>
  <script src="js/local_storage_manager.js"></script>
  <script src="js/game_manager.js"></script>
  <script src="js/application.js"></script>
  <script type="text/javascript">
  function pretty(time) {
  if (time < 0) {return "DNF";}
    var bits = time % 1000;
    time = (time - bits) / 1000;
    var secs = time % 60;
    var mins = ((time - secs) / 60) % 60;
    var hours = (time - secs - 60 * mins) / 3600;
    var s = "" + bits;
    if (bits < 10) {s = "0" + s;}
    if (bits < 100) {s = "0" + s;}
    s = secs + "." + s;
    if (secs < 10 && (mins > 0 || hours > 0)) {s = "0" + s;}
    if (mins > 0 || hours > 0) {s = mins + ":" + s;}
    if (mins < 10 && hours > 0) {s = "0" + s;}
    if (hours > 0) {s = hours + ":" + s;}
  return s;
}
  </script>
</body>
</html>
