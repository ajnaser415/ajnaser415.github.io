<head>
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css">
     <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
</head>
<body>
    <nav>
        <div class="nav-wrapper">
          <a href="#" class="brand-logo">Skin Cancer Diagnosis</a>
        </div>
      </nav>
<div style="padding:5%;">
        <h4 id="loadingmodel">Loading ML Model</h4>
        <div id="progressbar" class="progress">
            <div class="indeterminate"></div>
        </div>
        <div class="file-field input-field">
            <div class="btn">
              <span>Select Image</span>
              <input type="file" accept="image/*" onchange="onFileSelected(event)">
            </div>
            <div class="file-path-wrapper">
              <input class="file-path validate" type="text">
            </div>
          </div>
        <img id="image" width="100" height="75"></img>
        <br/>
        <br/>
        <a onclick="predict()" class="waves-effect waves-light btn">Classify Image</a>
    <h3>Prediction</h3>
        <b><p id="prediction"></p></b>
        <p id="probability"></p>
    </div>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/js/materialize.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@2.0.0/dist/tf.min.js"></script>
    <script src="static/js/skin_cancer_diagnosis_script.js"></script>
    <script>
        // Initialize our HTML elements as JS objects
        var imgtag = document.getElementById("image")
        var prediction_text = document.getElementById("prediction")
        var probability_text = document.getElementById("probability")
        var progressbar = document.getElementById("progressbar")
        var loadingmodel = document.getElementById("loadingmodel")
        //console.log(imgtag)
    </script>
</body>
