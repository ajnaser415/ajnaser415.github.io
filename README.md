</head>
<body>

    <!-- Title Bar -->
    <nav>
        <div class="nav-wrapper">
          <a href="#" class="brand-logo">Skin Cancer Diagnosis</a>
        </div>
      </nav>

    <!-- Contain for all other HTML Elements -->
    <div style="padding:5%;">

        <!-- Loading Bar -->
        <h4 id="loadingmodel">Loading ML Model</h4>
        <div id="progressbar" class="progress">
            <div class="indeterminate"></div>
        </div>

        <!-- Image File Input -->
        <div class="file-field input-field">
            <div class="btn">
              <span>Select Image</span>
              <input type="file" accept="image/*" onchange="onFileSelected(event)">
            </div>
            <div class="file-path-wrapper">
              <input class="file-path validate" type="text">
            </div>
          </div>
        
        <!-- Image to be Classified -->
        <img id="image" width="100" height="75"></img>

        <!-- Add New Lines -->

        <br/>
        <br/>
        
        <!-- Button to Perform Classification -->
        <a onclick="predict()" class="waves-effect waves-light btn">Classify Image</a>
        
        <!-- Text Fields for the Prediction and the Probability -->
        <h3>Prediction</h3>

        <b><p id="prediction"></p></b>
        <p id="probability"></p>

    </div>
        
    <!-- Import JS Libraries -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/js/materialize.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@2.0.0/dist/tf.min.js"></script>
    <script src="static/js/skin_cancer_diagnosis_script.js"></script>

    <!-- Javascript allows us to apply logic to our UI elements and programmatically control the website -->
    <!-- We'll be using Tensorflow JS to perform our model inference -->

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
