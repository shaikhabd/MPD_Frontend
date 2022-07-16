<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Molecule Editor</title>
    <script
      type="text/javascript"
      language="javascript"
      src="/JSME/jsme/jsme.nocache.js"
    ></script>
    <script>
      function jsmeOnLoad() {
        jsmeApplet = new JSApplet.JSME("jsme_container", "380px", "340px");
      }
    </script>
  </head>
  <body>
    <div id="jsme_container"></div>
    <button type="button" id="showSmiles">Show SMILES</button>
    <div id="outputSmiles"></div>
    <script>
      const showSmilesBtn = document.getElementById("showSmiles");
      const outputSmiles = document.getElementById("outputSmiles");
      showSmilesBtn.addEventListener("click", function () {
        outputSmiles.textContent = "";
        outputSmiles.textContent = jsmeApplet.smiles();
      });
    </script>
  </body>
</html>