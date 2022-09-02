## Кулькулятор расчета стоимости листовой печати для визиток
<div id="integratedCalculator" class="url-businesscards" style="position: relative; min-height: 150px;"></div>
<script>
    let container = document.getElementById("integratedCalculator");
    let  params = { 
            materialType: "sheet-printing",
        };
    let integrated = new PxpCalcManager(container, params);
</script>
<style>
    #integratedCalculator{width:44%;font-family:"Helvetica Neue",Helvetica,Arial,sans-serif; margin-top: 10px;min-width: 555px;}
    #integratedCalculator a,#integratedCalculator u{text-decoration:none;border-bottom:none;transition:.3s;line-height:1.5}
    #integratedCalculator ul{padding:0 0 0 20px;margin:0;width:100%}
    .url-businesscards #pxpProducCalc .material-selector>ul>li>ul>li a{width:150px;text-align:center;font-weight:400}
    .url-businesscards #pxpProducCalc .option-row.customWorkRadio .option-value label{width:150px}
    .url-businesscards #pxpProducCalc .option-value li>a{width:111px;text-align:center}
    .pxp-total-price.sticky-visible{z-index:2}
    #pxpProducCalc .pxp-total-price .sticky-block .info {display: block;}
    #pxpProducCalc.pxp-calculator .pxp-total-price .sticky-block .totalPriceContainer,#pxpProducCalc.pxp-calculator .pxp-total-price .sticky-block .totalPriceContainer+.buttons{margin:0;}
    .total-price__formatted {line-height: 22px;}
    #pxpProducCalc{border:1px solid #BBBDBE;margin:0;width:100%;padding:30px;border-radius:5px;margin-top:10px;margin-bottom:20px}
    #pxpProducCalc #pxpProducCalc{border:0 none;padding:0;margin:0}
    #pxpProducCalc .material-selector{margin:0}
    #pxpProducCalc .material-selector ul,#pxpProducCalc .custom-works ul{padding:0;list-style:none}
    #pxpProducCalc .option-value li,#pxpProducCalc .material-selector > ul > li > ul > li{float:left;margin:0 5px;position:relative}
    #pxpProducCalc .option-value li > a,#pxpProducCalc .custom-works label,#pxpProducCalc .material-selector > ul > li > ul > li a{color:#364657;border:1px solid #64BB46;border-radius:16px;padding:4px 12px;font-size:14px;display:block;transition:.3s;cursor:pointer}
    #pxpProducCalc .option-value li > a:hover,#pxpProducCalc .custom-works label:hover,#pxpProducCalc .material-selector > ul > li > ul > li a:hover{border:1px solid #EB6309;color:#fff;background:#EB6309}
    #pxpProducCalc .option-value li.selected > a,#pxpProducCalc .custom-works li.selected label,#pxpProducCalc .material-selector > ul > li > ul > li.selected a{color:#fff;background:#64BB46;border:1px solid #64BB46;display:inline-block}
    #pxpProducCalc .option-value li > a.calc-helper,#pxpProducCalc .material-selector > ul > li > ul > li a.calc-helper{width:20px;height:20px;position:absolute;top:-10px;right:-10px;line-height:16px;padding:0;vertical-align:middle;display:inline-block;background-color:#fff!important;border-radius:50%;text-align:center;margin-left:5px;color:#fff;border:2px solid!important;color:#666!important;font-weight:700}
    #pxpProducCalc .option-value li > .calc-helper-icon,#pxpProducCalc .material-selector > ul > li > ul > li .calc-helper-icon{position:absolute;bottom:50%;right:50%;transform:translate(50%,50%)}
    #pxpProducCalc .option-value li > a.calc-helper + .calc-helper-view,#pxpProducCalc .material-selector > ul > li > ul > li a.calc-helper + .calc-helper-view{visibility:hidden;position:absolute;max-width:20px;max-height:20px;top:-10px;right:-10px;background:#fff;padding:6px 8px;font-size:12px;line-height:1.2;z-index:2;border:2px solid #666;border-radius:10px;overflow:auto}
    #pxpProducCalc .option-value li > a.calc-helper:hover + .calc-helper-view,#pxpProducCalc .material-selector > ul > li > ul > li a.calc-helper:hover + .calc-helper-view,#pxpProducCalc .option-value li > a.calc-helper + .calc-helper-view:hover,#pxpProducCalc .material-selector > ul > li > ul > li a.calc-helper + .calc-helper-view:hover{visibility:visible;max-width:100%;max-height:360px}
    #pxpProducCalc .helper-container{position:relative}
    #pxpProducCalc .helper-container a.calc-helper{width:20px;height:20px;position:absolute;top:-10px;right:-10px;line-height:16px;padding:0;vertical-align:middle;display:inline-block;background-color:#fff!important;border-radius:50%;text-align:center;margin-left:5px;color:#fff;border:2px solid!important;color:#666!important;font-weight:700}
    #pxpProducCalc .helper-container .calc-helper-icon{position:absolute;bottom:50%;right:50%;transform:translate(50%,50%)}
    #pxpProducCalc .helper-container a.calc-helper + .calc-helper-view{visibility:hidden;position:absolute;max-width:20px;max-height:20px;top:-10px;right:-10px;background:#fff;padding:6px 8px;font-size:12px;line-height:1.2;z-index:2;border:2px solid #666;border-radius:10px;overflow:auto}
    #pxpProducCalc .helper-container a.calc-helper:hover + .calc-helper-view,#pxpProducCalc .helper-container a.calc-helper + .calc-helper-view:hover{visibility:visible;max-width:100%;max-height:360px}
    #pxpProducCalc .option-row .option-label{top:50%;font-weight:600;font-weight:600;font-size:16px;line-height:18px;display:block;margin-right:10px;color:#364657}
    #pxpProducCalc .option-row .option-value{list-style:none}
    #pxpProducCalc .option-row .option-value select{margin-top:10px;width:290px;height:30px;font-weight:400;color:#364657}
    #pxpProducCalc .option-row .option-value select:focus{outline:none}
    #pxpProducCalc .option-row .option-value > .list-inline{margin:0}
    #pxpProducCalc .list-inline > li{padding:0}
    #pxpProducCalc .material-selector > ul > li > ul > li{margin-top:14px}
    #pxpProducCalc .material-selector > ul > li > ul > li:first-child{margin-left:0}
    #pxpProducCalc .list-inline > li:first-child{margin-left:0}
    #pxpProducCalc .option-row{position:relative;margin-bottom:0;list-style:none;margin-bottom:20px}
    #pxpProducCalc .pxp-circulation-selector ul li:first-child{margin-left:0}
    #pxpProducCalc .option-row:after{content:'';display:block;clear:both}
    #pxpProducCalc a u{border-bottom:none 0}
    #pxpProducCalc .custom-works .formatted-price,#pxpProducCalc .custom-works .customworkitem,#pxpProducCalc .custom-works .formatted-price + span,#pxpProducCalc .custom-works .customworkitem + span,#pxpProducCalc .custom-works .custom-work-item-price + span{position:absolute;margin-left:-25px;margin-top:6px}
    #pxpProducCalc .radio input[type=radio],#pxpProducCalc .radio-inline input[type=radio],#pxpProducCalc .checkbox input[type=checkbox],#pxpProducCalc .checkbox-inline input[type=checkbox]{margin-left:0}
    #pxpProducCalc .custom-works ul li.customWorkRadio ul li .checkbox input[type="radio"]{position:absolute;left:35px}
    #pxpProducCalc .custom-works ul li.customWorkRadio ul li .checkbox{padding:0;display:inline-block}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox ul li .checkbox label{background:transparent;color:#000;border:0 none;float:left}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox ul li .checkbox span[data-bind="template:{name: template}"] input[type="checkbox"]{width:0}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox ul li .checkbox span:before{content:'';width:20px;height:20px;background:#fff;display:block;border-radius:50%;position:absolute;box-shadow:0 0 0 4px #F7F7F7;border:1px solid #eee;left:4px;right:auto;cursor:pointer;top:4px}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox ul li .checkbox{padding-left:0}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox ul li.selected .checkbox span:before{right:5px;left:auto;top:5px;background:#64BB46;cursor:pointer}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox ul li .checkbox span:after{content:'\000432\00043a\00043b.';position:absolute;right:5px;left:auto;top:3px;font-size:12px;color:#fff;cursor:pointer}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox ul li.selected .checkbox span:after{content:'\000432\00044b\00043a\00043b.';color:#fff;right:auto;left:8px;top:4px;cursor:pointer}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox ul li .checkbox span.formatted-price + span{width:70px;height:30px;margin-top:0;border-radius:16px;background:#BBBDBE;border:1px solid #BBBDBE;cursor:pointer;left:25px;position:relative;float:left}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox ul li.selected .checkbox span.formatted-price + span{border:#64BB46;background:#64BB46;cursor:pointer}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox .checkbox label{padding-left:30px!important;cursor:pointer}
    #pxpProducCalc .custom-works .customWorkRadio input[type="radio"]{display:none}
    #pxpProducCalc .custom-works .customWorkRadio .checkbox{padding:0}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox ul li .checkbox label:before{content:'';position:absolute;width:70px;height:30px;display:block;margin-left:-75px;margin-top:-4px}
    #pxpProducCalc .totalPriceContainer .price-per-photo{font-size:12px;margin:0 10px 0 0}
    #pxpProducCalc .editor-sizes.option-row input{width:100px;min-height:25px}
    #pxpProducCalc .editor-sizes.option-row .editor-sizes-width input{text-align:center}
    #pxpProducCalc .editor-sizes.option-row .editor-sizes-height input{text-align:center}
    #pxpProducCalc #totalPriceContainer+.buttons{width:auto;display:inline-block}
    #pxpProducCalc input[type=checkbox],#pxpProducCalc input[type=radio]{display:none}
    #pxpProducCalc .option-row.with-description .option-value.list-inline li{overflow:visible;position:relative;line-height:0}
    #pxpProducCalc .option-row.with-description .option-value.list-inline li label{width:100%;line-height:1.7;border-radius:4px;border:0}
    #pxpProducCalc .option-row.with-description .option-value.list-inline li label:after{content:'';position:absolute;top:0;bottom:0;left:0;right:0;z-index:1;border-radius:4px}
    #pxpProducCalc .option-row.large-format .option-value.list-inline li label:after{content:none}
    #pxpProducCalc .option-row.with-description .option-value.list-inline li.selected:hover,#pxpProducCalc .option-row.with-description .option-value.list-inline li.selected:hover .checkbox,#pxpProducCalc .option-row.with-description .option-value.list-inline li.selected:hover label:after{border-color:#64bb46}
    #pxpProducCalc .option-row.with-description .option-value.list-inline li.selected:hover .checkbox{border-bottom-color:#64bb46;background:#64bb46}
    #pxpProducCalc .option-row.with-description .option-value.list-inline li .customworkitem img{width:100%;padding:0;border-radius:15px}
    #pxpProducCalc .option-row li.selected label{display:inline-block;margin-bottom:0;border-radius:4px;padding:0;color:#fff;overflow:hidden;font-weight:400;background:#64bb46;border:1px solid #64bb46;max-width:210px}
    #pxpProducCalc .option-row li.selected:hover label{background:#64bb46;border:1px solid #64bb46}
    #pxpProducCalc .option-row li:hover label{background:#eb6309;border-color:#eb6309;color:#fff}
    #pxpProducCalc .option-row li label{display:inline-block;margin-bottom:0;width:100%;max-width:210px;background:0 0;border-radius:4px;padding:0;color:#000;overflow:hidden;font-weight:400;cursor:pointer;transition:.3s;text-align:center;border:1px solid #64bb46}
    #pxpProducCalc .option-row .option-value{list-style:none;min-height:35px;margin-left:0}
    #pxpProducCalc .option-row input#txtPartsQuantity,#pxpProducCalc .option-row input#txtQuantity{float:left;display:block;margin-top:0;width:180px}
    #pxpProducCalc .option-row input#txtQuantity,.activatedCoupons li{position:initial}
    #pxpProducCalc .option-row input+span.option-item-title{text-align:center;padding:5px 0 0;margin:0 auto;width:100%;float:left}
    #pxpProducCalc .option-row input#txtQuantity-for-calc2+span.measure{position:relative;margin:10px;top:0}
    #pxpProducCalc .option-row input+span.measure{position:relative;margin:10px;top:0}
    #pxpProducCalc .option-row.customWorkRadio .option-value label{min-height:inherit;padding:4px 15px;border:0}
    #pxpProducCalc .option-row .option-value label[for=txtPartsQuantity]{min-height:inherit}
    #pxpProducCalc .option-row .option-value label{background:0 0;color:#364657;width:auto;min-height:70px;line-height:1.7}
    #pxpProducCalc #totalPriceContainer,#pxpProducCalc .totalPriceContainer{float:none;padding:15px 0}
    #pxpProducCalc #totalPriceContainer+.buttons,#pxpProducCalc .totalPriceContainer+.buttons{float:none;margin-bottom:10px}
    #pxpProducCalc .material-selector>ul>li>ul>li,#pxpProducCalc .option-value li{float:left;margin:0 10px 5px 0}
    #pxpProducCalc .material-selector>ul>li>ul>li .option-item-description{width:100%;position:relative;top:4px}
    #pxpProducCalc .option-row .option-value select{margin-top:0!important;width:280px}
    #pxpProducCalc .material-selector .option-row .option-label,#pxpProducCalc .material-selector>ul>li>ul>li a.calc-helper+.calc-helper-view ol li,#pxpProducCalc .material-selector>ul>li>ul>li a.calc-helper+.calc-helper-view ul li,#pxpProducCalc .option-row .option-label,#pxpProducCalc .option-value li>a.calc-helper+.calc-helper-view ol li,#pxpProducCalc .option-value li>a.calc-helper+.calc-helper-view ul li{margin-bottom:10px}
    .with-bg-gray #pxpProducCalc{background-color:#fefefe;border-color:#ddd}
    .with-bg-gray .pxp-total-price .sticky-block{background:#ddd}
    #pxpProducCalc .measure{margin-left:10px}
    #pxpProducCalc{position:relative;min-height:140px;margin-top:0}
    #pxpProducCalc .calc-lock{position:absolute;top:0;bottom:0;left:0;right:0;background:rgba(255,255,255,.6);width:100%;height:100%;z-index:1}
    #pxpProducCalc .calc-lock div{display:block;text-align:center;position:absolute;left:calc(50% - 125px);top:calc(50% - 55px);-ms-transform:translate(-50%,-50%);-o-transform:translate(-50%,-50%);background:#fff;width:250px;height:110px;padding:10px;border:1px solid #ddd;border-radius:5px;box-shadow:0 0 10px 1px rgba(0,0,0,.2)}
    #pxpProducCalc .calc-lock div span{margin-top:55px;display:block}
    #pxpProducCalc .calc-lock div:before{content:"";animation:a 1s linear infinite;border:4px solid #eee;border-left-color:#64bb46;border-radius:50%;display:inline-block;margin:-40px 0 0 -20px;height:40px;width:40px;left:50%;top:50%;position:absolute}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox ul li .checkbox span[data-bind="template:{name:template}"] input[type=checkbox]{width:0;display:none}
    #pxpProducCalc .custom-works .customWorkDropdown label,#pxpProducCalc .custom-works .customWorkDropdown label:hover{padding:0;border:0;background:0 0;color:#364657;cursor:auto}
    #pxpProducCalc .custom-works .customWorkDropdown .option-value select+div>span{color:#000;font-weight:600;float:left;padding:14px}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li:hover .checkbox,#pxpProducCalc .custom-works ul li.customWorkRadio ul li:hover .checkbox,#pxpProducCalc .option-row.with-description .option-value.list-inline li:hover .checkbox{background:#eb6309;border-color:#eb6309}
    #pxpProducCalc .custom-works ul li.customWorkRadio ul li:hover .checkbox label{color:#fff;border:0}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li.selected .checkbox,#pxpProducCalc .custom-works ul li.customWorkRadio ul li.selected .checkbox,#pxpProducCalc .custom-works ul li.customWorkRadio ul li.selected:hover .checkbox{background:#64bb46;border-color:#64bb46}
    #pxpProducCalc .custom-works ul li.customWorkRadio ul li .checkbox{padding:0;margin-top:0;width:100%;line-height:0;margin-bottom:0;background:#fff;transition:.3s;border-radius:4px;border:1px solid #64bb46}
    #pxpProducCalc .custom-work-item-price,#pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li .checkbox span.formatted-price+span:after,#pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li .checkbox span.formatted-price+span:before,#pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li.selected .checkbox span.formatted-price+span:after,#pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li.selected .checkbox span.formatted-price+span:before,#pxpProducCalc .custom-works ul li.no-description ul li .note.customworkitem,.shc.sh_btn img.shc.sh_logo_btn.sh_logo_img{display:none}
    #pxpProducCalc .custom-works .note.customworkitem{position:relative;border:1px solid #64bb46;border-radius:15px;margin:15px 0 0}
    #pxpProducCalc .custom-works .note.customworkitem:before{color:#fff;content:"▲";left:50%;line-height:20px;position:absolute;top:-15px;text-shadow:1px -2px 0 #64bb46,-1px -2px 0 #64bb46,0 -4px 0 #64bb46;font-size:16px;-webkit-transform:translate(-30%,0);transform:translate(-30%,0);-moz-transform:translate(-30%,0)}
    #pxpProducCalc .custom-works .for-stamps .note img{width:60%}
    #pxpProducCalc span.price-per-item{display:inline-block;margin-top:5px;font-size:12px}
    #pxpProducCalc .option-row .option-value label[for=txtQuantity]{line-height:1.7;min-height:0}
    #pxpProducCalc .option-row .option-value input#txtQuantity-for-calc2,#pxpProducCalc .option-row .option-value label[for=txtQuantity] input#txtQuantity{position:relative;width:180px}
    #pxpProducCalc .option-row .option-value label[for=txtQuantity] input#txtQuantity+span.measure{float:left;margin-top:-10px}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox.alone ul li .checkbox label{border-radius:0;padding:4px 10px;line-height:1.2;display:inline-block;min-height:45px;min-width:210px}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li .checkbox span.formatted-price+span{width:auto;background:0 0;border:0}
    #pxpProducCalc .alone.monotony-option .list-inline>li,#pxpProducCalc .alone.monotony-option .list-inline>li:hover{border:unset}
    #pxpProducCalc .alone.monotony-option .option-label{display:block!important}
    #pxpProducCalc .alone.monotony-option .list-inline>li .checkbox{margin-top:0;border-radius:3px;min-height:33px;margin-bottom:0}
    #pxpProducCalc .alone.monotony-option .list-inline>li .note.customworkitem a.shipping-trigger{padding:4px}
    #pxpProducCalc .alone.monotony-option .list-inline>li.checkbox{margin:0!important}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li.selected .checkbox span.formatted-price+span{background:0 0;color:#fff;width:100%;height:auto}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li .checkbox{background:0 0;border:1px solid #64bb46;transition:.3s}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li .checkbox label{width:100%;padding:3px 15px!important;min-height:initial;line-height:1.7;border-color:transparent}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option.with-description ul li.selected .checkbox label{border-radius:3px}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li label{border:1px solid #64bb46}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li,#pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li.selected{background:0 0;border:0;border-radius:3px}
    #pxpProducCalc .custom-works ul li.customWorkCheckbox.alone.monotony-option ul li.selected label{color:#fff;background:0 0}
    #pxpProducCalc .custom-works li.selected .checkbox{color:#fff;background:#64bb46}
    #pxpProducCalc .custom-works li.selected label,#pxpProducCalc .material-selector>ul>li>ul>li.selected a,#pxpProducCalc .option-value li.selected>a{color:#fff;background:#64bb46;border:1px solid #64bb46;display:inline-block}
    #pxpProducCalc .custom-works label,#pxpProducCalc .material-selector>ul>li>ul>li a,#pxpProducCalc .option-value li>a{color:#364657;border:1px solid #64bb46;border-radius:4px;padding:4px 12px;font-size:14px;display:block;transition:.3s;cursor:pointer}
    #customWorksContainer .a-book-color ul,.swiper-container.random_template{margin:0 -15px}
    #pxpProducCalc ol li,#pxpProducCalc ul li{margin:0 0 30px}
    #pxpProducCalc .option-row .option-value label[for="integratedCalculator-txtQuantity"] input#integratedCalculator-txtQuantity{position:relative;margin-top:0;float:left}
    #pxpProductCalc label{display:inline-block;margin-bottom:5px;font-weight:700}
    #pxpProducCalc .option-row .option-value label[for="integratedCalculator-txtQuantity"]{padding:0;line-height:1.7;min-height:0}
    #pxpProducCalc .option-row input#txtPartsQuantity,#pxpProducCalc .option-row input#integratedCalculator-txtQuantity{float:left;display:block;margin-top:0;width:180px}
    #pxpProducCalc .option-row .option-value input#txtQuantity-for-calc2,#pxpProducCalc .option-row .option-value label[for=integratedCalculator-txtQuantity] input#integratedCalculator-txtQuantity{position:relative;width:180px;font-weight:700;min-height:39px}
    #pxpProducCalc .option-row .option-value label[for=integratedCalculator-txtQuantity] input#integratedCalculator-txtQuantity+span.measure{float:left;margin-top:9px;font-weight:700;font-size:14px}
    /* .pxp-total-price .btn{margin-left:15px} */
    #pxpProducCalc .pxp-calculator .pxp-total-price .totalPriceContainer,#pxpProducCalc.pxp-calculator .pxp-total-price .totalPriceContainer+.buttons{margin:0 0 10px}
    #pxpProducCalc .buttons .ok,#pxpProducCalc .buttons .ok-disabled{display:inline-block}
    #pxpProducCalc a.btn:active{background:0 0 #64bb46;box-shadow:1px 1px 1px #18410a inset}
    #pxpProducCalc .btn,#pxpProducCalc a.btn{border:0;display:inline-block;font-size:18px;font-weight:400;padding:5px 15px;border-radius:4px;outline:0;box-shadow:none;text-shadow:none;background:#64bb46;color:#fff;border:1px solid transparent}
    #pxpProducCalc .btn:hover,#pxpProducCalc a.btn:hover{background:0 0 #eb6309}
    #pxpProducCalc.pxp-calculator .pxp-total-price .totalPriceContainer{margin:0 0 10px}
    #pxpProducCalc .totalPriceContainer,#pxpProducCalc .totalPriceContainer span.price-total{width:100%}
    .totalPriceContainer .price-per-item{padding:0 0 0 .4em}
    #integratedCalculator .pxp_calc_quick_order_manager_block_info_text a{border-bottom:1px solid #64bb46;font-weight:400}
    #integratedCalculator .currency.rub:before{content:"₽ ";font-size:1.06em}
    .url-businesscards #pxpProducCalc .pxp-circulation-selector ul li.circulation-selector__item.option-row {margin-bottom: 25px;}
    .url-businesscards #pxpProducCalc .custom-works__list .option-row:first-child {margin-bottom: 15px;}
    #pxpProducCalc a.btn:last-child {display: none}
        @media screen and (max-width: 1055px) {
        #integratedCalculator {width:50%; min-width: 400px;}
    }
    @media (max-width: 992px) {
        #pxpProducCalc .sticky-block .info span.price-per-item{display:none;}
    }
    @media screen and (max-width: 800px) {
        #integratedCalculator {width: 100%; min-width: auto;}
    }
    @media screen and (max-width: 768px) {
        .url-businesscards .block-address{margin-bottom:15px}
        .pxp-total-price .sticky-block{height:55px}
    }
    @media screen and (max-width:571px) {
        .url-businesscards #pxpProducCalc .material-selector>ul>li>ul>li a{width:135px}
        .url-businesscards #pxpProducCalc ul li.customWorkRadio:first-child .option-value label,.url-businesscards #pxpProducCalc ul li.customWorkRadio:nth-child(2) .option-value label{width:135px}
    }
    @media (max-width: 414px) {
        .pxp-total-price .sticky-block .info {margin: 0 10px;}
        #pxpProducCalc.pxp-calculator .pxp-total-price .sticky-block .totalPriceContainer{font-size:14pt}
    }
    @media (max-width: 340px) {
        #pxpProducCalc.pxp-calculator .pxp-total-price .sticky-block .totalPriceContainer{font-size:10pt}
    }
</style>