<template>
  <div>
    <div style="text-align: center;margin-top: 5px">
      <button class="wlt button">按钮</button>
      <button class="wlt focus button">按钮</button>
      <button class="wlt active button">按钮</button>
      <button class="wlt button" disabled>按钮</button>
      <button class="wlt disabled button">按钮</button>
    </div>
    <div style="text-align: center;margin-top: 5px">
      <button class="wlt primary button">按钮</button>
      <button class="wlt success button">按钮</button>
      <button class="wlt warning button">按钮</button>
      <button class="wlt danger button">按钮</button>
      <button class="wlt info button">按钮</button>
    </div>
    <div style="text-align: center;margin-top: 5px">
      <button class="wlt primary mini button">按钮</button>
      <button class="wlt success small button">按钮</button>
      <button class="wlt warning medium button">按钮</button>
      <button class="wlt danger button">按钮</button>
    </div>
    <!--<button class="wlt gradient button">按钮</button>-->
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
  // Button sizes
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
      }
    }
    .badge {
      color: $background;
      background-color: $color;
    }
  }
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
  /*******************************
              default button
  *******************************/
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
  /*******************************
              primary button
  *******************************/
  .wlt.primary.button{
    @include button-variant($primaryBtnColor,$primaryBtnBgColor,$primaryBtnBorderColor);
  }
  /*******************************
              success button
  *******************************/
  .wlt.success.button{
    @include button-variant($successBtnColor,$successBtnBgColor,$successBtnBorderColor);
  }
  /*******************************
              warning button
  *******************************/
  .wlt.warning.button{
    @include button-variant($warningBtnColor,$warningBtnBgColor,$warningBtnBorderColor);
  }
  /*******************************
              danger button
  *******************************/
  .wlt.danger.button{
    @include button-variant($dangerBtnColor,$dangerBtnBgColor,$dangerBtnBorderColor);
  }
  /*******************************
              info button
  *******************************/
  .wlt.info.button{
    @include button-variant($infoBtnColor,$infoBtnBgColor,$infoBtnBorderColor);
  }
  /*******************************
              mini button
  *******************************/
  .wlt.mini.button,
  .wlt.primary.mini.button,
  .wlt.success.mini.button,
  .wlt.warning.mini.button,
  .wlt.danger.mini.button,
  .wlt.info.mini.button {
    @include button-size(7px,15px,12px,12px,3px);
  }
  /*******************************
                small button
    *******************************/
  .wlt.small.button,
  .wlt.primary.small.button,
  .wlt.success.small.button,
  .wlt.warning.small.button,
  .wlt.danger.small.button,
  .wlt.info.small.button {
    @include button-size(9px,15px,12px,12px,3px);
  }
  /*******************************
              medium button
  *******************************/
  .wlt.medium.button,
  .wlt.primary.medium.button,
  .wlt.success.medium.button,
  .wlt.warning.medium.button,
  .wlt.danger.medium.button,
  .wlt.info.medium.button {
    @include button-size(10px,20px,14px,14px,4px);
  }

  .wlt.gradient.button{
    /*IE 6 7 8*/
    filter: progid:DXImageTransform.Microsoft.Gradient(gradientType=0, startColorStr=#AC07BD, endColorStr=#f6f6f8);
    /* IE 10 */
    background: -ms-linear-gradient(top, #AC07BD, #f6f6f8);
    /*火狐*/
    background:-moz-linear-gradient(top, #AC07BD, #f6f6f8);
    /* Safari 4-5, Chrome 1-9*/
    background: -webkit-gradient(linear, 0% 0%, 0% 100%, from(#AC07BD), to(#f140f8));
    /*Safari5.1 Chrome 10+*/
    background: -webkit-linear-gradient(top, #AC07BD, #f140f8);
    /*Opera 11.10+*/
    background: -o-linear-gradient(top, #AC07BD, #f140f8);
    /* Standard syntax; must be last */
    background:linear-gradient(to bottom, hsl(0, 80%, 70%), #bada55);
  }

</style>
