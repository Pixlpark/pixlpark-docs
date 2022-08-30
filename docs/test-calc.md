## Кулькулятор расчета стоимости листовой печати для визиток
<div id="integratedCalculator"></div>
<!-- <script>window.pxp.frontend = null</script> -->
<script src="//demo.pixlpark.ru/api/calc/externalCalc"></script>
<script>window.pxp.frontend = null</script>
<script>
  var container = document.getElementById("integratedCalculator");
  console.log(123);
  var params = { 
		materialType: "sheet-printing",
		material: '1005705',
        origin: 'https://demo.pixlpark.ru',
	};
  var integrated = new PxpCalcManager(container, params);
</script>
