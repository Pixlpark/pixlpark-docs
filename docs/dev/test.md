# Встроенный калькулятор
<div id="container"></div>
<script src="http://demo.pixlpark.ru/api/calc/externalCalc"></script>
<script>
  var container = document.getElementById("container");
  var params = { materialType: "framed-canvases" };
  var integrated = new PxpCalcManager(container, params);
</script>