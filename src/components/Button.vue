<template>
  <div>
    <div style="text-align: center;margin-top: 5px;font-size:0;">
      <a class="wlt button" href="#">连接按钮</a><button class="wlt button">默认按钮</button>
      <button class="wlt focus button">focus按钮</button>
      <button class="wlt active button">active按钮</button>
      <button class="wlt button" disabled>disabled按钮</button>
      <button class="wlt disabled button">disabled按钮</button>
    </div>
    <div style="text-align: center;margin-top: 5px;font-size:0;">
      <button class="wlt primary button">primary按钮</button>
      <button class="wlt success button">success按钮</button>
      <button class="wlt warning button">warning按钮</button>
      <button class="wlt danger button">danger按钮</button>
      <button class="wlt info button">info按钮</button>
    </div>
    <div style="text-align: center;margin-top: 5px;font-size:0;">
      <button class="wlt link primary button">连接按钮</button>
      <button class="wlt link success button">连接按钮</button>
      <button class="wlt link warning button">连接按钮</button>
      <button class="wlt link danger button">连接按钮</button>
      <button class="wlt link info button">连接按钮</button>
    </div>
    <div style="text-align: center;margin-top: 5px;font-size:0;">
      <button class="wlt primary mini button">mini按钮</button>
      <button class="wlt success small button">small按钮</button>
      <button class="wlt warning medium button">medium按钮</button>
      <button class="wlt danger button">按钮</button>
    </div>
    <div style="width: 400px;margin: 0 auto;font-size:0;">
      <button class="wlt block button">整行按钮</button>
      <button class="wlt block primary button">整行按钮</button>
      <button class="wlt block success button">整行按钮</button>
      <button class="wlt block warning button">整行按钮</button>
      <button class="wlt block danger button">整行按钮</button>
      <button class="wlt block info button">整行按钮</button>
    </div>
    <div style="text-align: center;margin-top: 5px;font-size:0;">
      <button class="wlt weight button">加粗按钮</button>
      <button class="wlt weight primary button">加粗按钮</button>
      <button class="wlt weight success button">加粗按钮</button>
      <button class="wlt weight warning button">加粗按钮</button>
      <button class="wlt weight danger button">加粗按钮</button>
      <button class="wlt weight info button">加粗按钮</button>
    </div>
    <div style="text-align: center;margin-top: 5px;font-size:0;">
      <button class="wlt radius weight button">半圆角按钮</button>
      <button class="wlt radius weight primary button">半圆角按钮</button>
      <button class="wlt radius weight success button">半圆角按钮</button>
      <button class="wlt radius weight warning button">半圆角按钮</button>
      <button class="wlt radius weight danger button">半圆角按钮</button>
      <button class="wlt radius weight info button">半圆角按钮</button>
    </div>
    <div style="text-align: center;margin-top: 5px;font-size:0;">
      <button class="wlt shadow weight button">阴影按钮</button>
      <button class="wlt shadow weight primary button">阴影按钮</button>
      <button class="wlt shadow weight success button">阴影按钮</button>
      <button class="wlt shadow weight warning button">阴影按钮</button>
      <button class="wlt shadow weight danger button">阴影按钮</button>
      <button class="wlt shadow weight info button">阴影按钮</button>
    </div>
    <div style="text-align: center;margin-top: 5px;font-size:0;">
      <button class="wlt primary gradient button">效果按钮</button>
      <button class="wlt success gradient button">效果按钮</button>
      <button class="wlt warning gradient button">效果按钮</button>
      <button class="wlt danger gradient button">效果按钮</button>
      <button class="wlt info gradient button">效果按钮</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Button',
  data () {
    return {
    }
  }
}
</script>

<style scoped lang="scss">
  /*****- 自定义 -*****/
  @mixin radius($radius){
     -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
     border-radius: $radius;
     }
  // Button sizes
  @mixin linear-gradient-top($from, $to) {
    background: $to;
    /*IE 6 7 8*/
    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr=$from, endColorstr=$to,GradientType=0 );
    /*火狐*/
    background: -moz-linear-gradient(top,  $from, $to);
    /* WebKit (Chrome 11+) */
    background: -webkit-gradient(linear, left top, left bottom, color-stop(0%,$from), color-stop(100%,$to));
    /* WebKit (Safari 5.1+, Chrome 10+) */
    background: -webkit-linear-gradient(top,  $from,$to);
    /* Opera */
    background: -o-linear-gradient(top, $from,$to);
    /* IE 10 */
    background: -ms-linear-gradient(top,  $from,$to);
    /* W3C */
    background: linear-gradient(to bottom, $from,$to);
  }
  @mixin linear-gradient-left($from, $to) {
    background: $to;
    /*IE 6 7 8*/
    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr=$from, endColorstr=$to,GradientType=0 );
    /*火狐*/
    background: -moz-linear-gradient(left,  $from, $to);
    /* WebKit (Chrome 11+) */
    background: -webkit-gradient(linear, top left, top right, color-stop(0%,$from), color-stop(100%,$to));
    /* WebKit (Safari 5.1+, Chrome 10+) */
    background: -webkit-linear-gradient(left,  $from,$to);
    /* Opera */
    background: -o-linear-gradient(left, $from,$to);
    /* IE 10 */
    background: -ms-linear-gradient(left,  $from,$to);
    /* W3C */
    background: linear-gradient(to right, $from,$to);
  }
  @mixin button-size($padding-vertical, $padding-horizontal, $font-size, $line-height, $border-radius) {
    padding: $padding-vertical $padding-horizontal;
    font-size: $font-size;
    line-height: $line-height;
    border-radius: $border-radius;
  }
  @mixin button-variant($color, $background, $border) {
    color: $color;
    background-color: $background;
    border-color: $border;
    &:focus,
    &.focus {
      color: $color;
      background-color: darken($background, 10%);
      border-color: darken($border, 5%);
    }
    &:hover {
      color: $color;
      background-color: darken($background, 10%);
      border-color: darken($border, 10%);
    }
    &:active,
    &.active,
    .open > &.dropdown-toggle {
      color: $color;
      background-color: darken($background, 10%);
      border-color: darken($border, 15%);
      background-image: none;
      &:hover,
      &:focus,
      &.focus {
        color: $color;
        background-color: darken($background, 17%);
        border-color: darken($border, 25%);
      }
    }
    &.disabled,
    &[disabled],
    fieldset[disabled] & {
      &:hover,
      &:focus,
      &.focus {
        background-color: $background;
        border-color: $border;
        cursor: not-allowed;
        text-decoration: none!important;
      }
    }
    .badge {
      color: $background;
      background-color: $color;
    }
  }
  @mixin button-variant-gradient($color, $lcolor ,$rcolor, $border) {
    @include linear-gradient-left($lcolor, $rcolor);
    &:focus,
    &.focus {
      color: $color;
      background-color: darken($lcolor, 10%);
      border-color: darken($border, 5%);
    }
    &:hover {
      color: $color;
      background-color: darken($lcolor, 10%);
      border-color: darken($border, 10%);
    }
    &:active,
    &.active,
    .open > &.dropdown-toggle {
      color: $color;
      background-color: darken($lcolor, 10%);
      border-color: darken($border, 15%);
      background-image: none;
      &:hover,
      &:focus,
      &.focus {
        color: $color;
        background-color: darken($lcolor, 17%);
        border-color: darken($border, 25%);
      }
    }
    &.disabled,
    &[disabled],
    fieldset[disabled] & {
      &:hover,
      &:focus,
      &.focus {
        background-color: $lcolor;
        border-color: $border;
        cursor: not-allowed;
        text-decoration: none!important;
      }
    }
    .badge {
      color: $lcolor;
      background-color: $color;
    }
  }
  :root .gradient{filter:none;}
  $defaultBtnColor: #606266;
  $defaultBtnBgColor: #FFFFFF;
  $defaultBtnBorderColor: #DCDFE6;
  $primaryBtnColor: #FFFFFF;
  $primaryBtnBgColor: #409EFF;
  $primaryBtnBorderColor: #409EFF;
  $successBtnColor: #FFFFFF;
  $successBtnBgColor: #67C23A;
  $successBtnBorderColor: #67C23A;
  $warningBtnColor: #FFFFFF;
  $warningBtnBgColor: #E6A23C;
  $warningBtnBorderColor: #E6A23C;
  $dangerBtnColor: #FFFFFF;
  $dangerBtnBgColor: #F56C6C;
  $dangerBtnBorderColor: #F56C6C;
  $infoBtnColor: #FFFFFF;
  $infoBtnBgColor: #909399;
  $infoBtnBorderColor: #909399;
  /*****- default button -*****/
  .wlt.button{
    cursor: pointer;
    display: inline-block;
    min-height: 14px;
    font-size: 14px;
    outline: none;
    border: 1px solid #DCDFE6;
    vertical-align: baseline;
    background: #FFFFFF none;
    color: #000000;
    font-family: 'Lato', 'Helvetica Neue', Arial, Helvetica, sans-serif;
    margin: 0;
    padding: 12px 20px;
    text-transform: none;
    text-shadow: none;
    font-weight: none;
    line-height: 1;
    font-style: normal;
    text-align: center;
    text-decoration: none;
    border-radius: 4px;
    -webkit-box-shadow: 0px 0px 0px 1px transparent inset, 0px 0em 0px 0px rgba(34, 36, 38, 0.15) inset;
    box-shadow: 0px 0px 0px 1px transparent inset, 0px 0em 0px 0px rgba(34, 36, 38, 0.15) inset;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    -webkit-transition: opacity 0.1s ease, background-color 0.1s ease, color 0.1s ease, background 0.1s ease, -webkit-box-shadow 0.1s ease;
    transition: opacity 0.1s ease, background-color 0.1s ease, color 0.1s ease, background 0.1s ease, -webkit-box-shadow 0.1s ease;
    transition: opacity 0.1s ease, background-color 0.1s ease, color 0.1s ease, box-shadow 0.1s ease, background 0.1s ease;
    transition: opacity 0.1s ease, background-color 0.1s ease, color 0.1s ease, box-shadow 0.1s ease, background 0.1s ease, -webkit-box-shadow 0.1s ease;
    will-change: '';
    -webkit-tap-highlight-color: transparent;
    @include button-variant($defaultBtnColor,$defaultBtnBgColor,$defaultBtnBorderColor);
  }
  /*****-  primary button -*****/
  .wlt.primary.button{
    @include button-variant($primaryBtnColor,$primaryBtnBgColor,$primaryBtnBorderColor);
  }
  /*****- success button -*****/
  .wlt.success.button{
    @include button-variant($successBtnColor,$successBtnBgColor,$successBtnBorderColor);
  }
  /*****- warning button -*****/
  .wlt.warning.button{
    @include button-variant($warningBtnColor,$warningBtnBgColor,$warningBtnBorderColor);
  }
  /*****- danger button -*****/
  .wlt.danger.button{
    @include button-variant($dangerBtnColor,$dangerBtnBgColor,$dangerBtnBorderColor);
  }
  /*****- info button -*****/
  .wlt.info.button{
    @include button-variant($infoBtnColor,$infoBtnBgColor,$infoBtnBorderColor);
  }
  /*****- mini button -*****/
  .wlt.mini.button,
  .wlt.primary.mini.button,
  .wlt.success.mini.button,
  .wlt.warning.mini.button,
  .wlt.danger.mini.button,
  .wlt.info.mini.button {
    @include button-size(7px,15px,12px,12px,3px);
  }
  /*****- small button -*****/
  .wlt.small.button,
  .wlt.primary.small.button,
  .wlt.success.small.button,
  .wlt.warning.small.button,
  .wlt.danger.small.button,
  .wlt.info.small.button {
    @include button-size(9px,15px,12px,12px,3px);
  }
  /*****- medium button -*****/
  .wlt.medium.button,
  .wlt.primary.medium.button,
  .wlt.success.medium.button,
  .wlt.warning.medium.button,
  .wlt.danger.medium.button,
  .wlt.info.medium.button {
    @include button-size(10px,20px,14px,14px,4px);
  }
   /*****- link button -*****/
  .wlt.link.button{
    &:hover{
      text-decoration: underline;
    }
  }
   /*****- block button -*****/
  .wlt.block.button{
    display: block;
    width: 100%;
  }
  .wlt.block.button+.wlt.block.button{
    margin-left: 0px;
  }
  .wlt.button + .wlt.button{
    margin-left: 5px;
  }
  .wlt.block.button + .wlt.block.button{
    margin-top: 5px;
  }
  /*****- weight button -*****/
  .wlt.weight.button{
    font-weight: 700;
  }
  /*****- radius button -*****/
  .wlt.radius.button{
    @include radius(50px);
  }
  /*****- shadow button -*****/
  .wlt.shadow.button{
    box-shadow: 1px 1px 4px 0px #ece1e1;
  }
  /*****- primary gradient button -*****/
  .wlt.primary.gradient.button{
    @include button-variant-gradient(#ffffff, #409EFF ,#4fbaff, #409EFF);
  }
  /*****- success gradient button -*****/
  .wlt.success.gradient.button{
    @include button-variant-gradient(#ffffff, #67C23A ,#58ea00, #67C23A);
  }
  /*****- warning gradient button -*****/
  .wlt.warning.gradient.button{
    @include button-variant-gradient(#ffffff, #E6A23C ,#ffb74c, #E6A23C);
  }
  /*****- danger gradient button -*****/
  .wlt.danger.gradient.button{
    @include button-variant-gradient(#ffffff, #F56C6C ,#ff8181, #F56C6C);
  }
  /*****- info gradient button -*****/
  .wlt.info.gradient.button{
    @include button-variant-gradient(#ffffff, #909399 ,#a9adaf, #909399);
  }
  .wlt.transition.button{
    transition:color 2s;
    -webkit-transition:color 2s; /* Safari */
  }

</style>
