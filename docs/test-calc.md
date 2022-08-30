## Кулькулятор расчета стоимости листовой печати для визиток
<div id="integratedCalculator"></div>
<script>window.pxp.frontend = null</script>
<script src="https://demo.pixlpark.ru/api/calc/externalCalc"></script>
<script>
  var container = document.getElementById("integratedCalculator");
  var params = { 
		materialType: "sheet-printing",
		material: '1005705',
	};
  var integrated = new PxpCalcManager(container, params);
</script>