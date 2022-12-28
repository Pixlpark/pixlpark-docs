## Калькулятор расчета стоимости листовой печати для визиток

<!-- <div id="merchCalculator"></div>
<script>
    var settings = {
    merchId: 977,
    merchVariantId: 63163,
    };
    console.log(1);
   MerchPageManager("merchCalculator", settings);
</script> -->

<div id="integratedCalculator" class="url-prints" style="position: relative; min-height: 150px;"></div>
<script>
    let container = document.getElementById("integratedCalculator");
    let  params = {
            materialType: "3d-letters",
        };
    let integrated = new PxpCalcManager(container, params);
</script>
<style>
    .loading-wheel:before{position:absolute;top:50%;left:50%;content:'';z-index:1112;display:block;width:32px;height:32px;margin:-16px 0 0 -16px;border:2px solid rgb(117,117,117);border-radius:50%;border-left-color:transparent;border-right-color:transparent;animation:cssload-spin 500ms infinite linear;-o-animation:cssload-spin 500ms infinite linear;-ms-animation:cssload-spin 500ms infinite linear;-webkit-animation:cssload-spin 500ms infinite linear;-moz-animation:cssload-spin 500ms infinite linear}
    .loading-wheel:after{position:absolute;top:0;left:0;bottom:0;right:0;content:'';background:#fff;z-index:1111;opacity:.9;display:block}
</style>
