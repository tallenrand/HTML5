<!DOCTYPE html>

<!--
     HTML code used with Epic Games HTML5 projects

     much of this is for UE4 development purposes.

     to create a custom HTML file for your project:
     - make a copy of this file - or make one from scratch
     - and put it in: "your project folder"/Build/HTML/GameX.html.template
-->

<html lang="en">
<head>
	<title>Cards_Test</title>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">

	<script src="https://code.jquery.com/jquery-2.1.3.min.js"></script>
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.4/js/bootstrap.min.js"></script>
	<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.4/css/bootstrap.min.css" rel="stylesheet">

	<link href="Cards_Test.css" rel="stylesheet">
</head>
<body>

<div class="wrapper" id="mainarea">
	<div class="alert alert-warning centered-axis-xy" style="min-height: 20px; display:none;" role="alert" id="compilingmessage">
		<div id='loadTasks'> </div>
	</div>
	<canvas id="canvas" class="emscripten" oncontextmenu="event.preventDefault()" style="display:none;">
</div>
<div class="row buttonarea text-center" id="buttonrow">
	<div class="col-sm-2 text-center"></div>
	<div class="col-sm-2 text-center"><button type="button" class="btn btn-primary" onclick="Module['pauseMainLoop']();">Pause</button></div>
	<div class="col-sm-2 text-center"><button type="button" class="btn btn-primary" onclick="Module['resumeMainLoop']();">Resume</button></div>
	<div class="col-sm-2 text-center"></div>
	<div class="col-sm-2 text-center"><button type="button" class="btn btn-primary" id='clear_indexeddb' onclick="deleteIndexedDBStorage();">Clear IndexedDB</button></div>
	<div class="col-sm-2 text-center"><button type="button" class="btn btn-primary" id="fullscreen_request">FullScreen</button></div>
	<div class="col-sm-2 text-center"></div>
	<div class="col-sm-2 text-center"></div>
</div>
<div class="texthalf text-normal jumbotron " id="logwindow" style='display:none'></div>

<script src="Cards_Test.UE4.js"></script>
</body>
</html>
