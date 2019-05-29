<template>
  <div style="text-align: center;margin-top: 100px">
    <button class="wlt active button">按钮</button>
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
  /*******************************
              button
  *******************************/
  .wlt.button{
    cursor: pointer;
    display: inline-block;
    min-height: 1em;
    outline: none;
    border: none;
    vertical-align: baseline;
    background: #E0E1E2 none;
    color: rgba(0, 0, 0, 1);
    font-family: 'Lato', 'Helvetica Neue', Arial, Helvetica, sans-serif;
    margin: 0em 0.25em 0em 0em;
    padding: 0.78571429em 1.5em 0.78571429em;
    text-transform: none;
    text-shadow: none;
    font-weight: none;
    line-height: 1em;
    font-style: normal;
    text-align: center;
    text-decoration: none;
    border-radius: 0.28571429rem;
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
    /*hover*/
    &:hover{
      background-color: #CACBCD;
      color: rgba(0, 0, 0, 0.8);
      background-image: none;
      -webkit-box-shadow: 0px 0px 0px 1px transparent inset, 0px 0em 0px 0px rgba(34, 36, 38, 0.15) inset;
      box-shadow: 0px 0px 0px 1px transparent inset, 0px 0em 0px 0px rgba(34, 36, 38, 0.15) inset;
      .icon{
        opacity: 0.85;
      }
    }
    /*focus*/
    &:focus {
      background-color: #CACBCD;
      color: rgba(0, 0, 0, 0.8);
      background-image: '' !important;
      -webkit-box-shadow: '' !important;
      box-shadow: '' !important;
      .icon {
        opacity: 0.85;
      }
    }
    /*active*/
    &:active{
      background-color: #BABBBC;
      background-image: '';
      color: rgba(0, 0, 0, 0.9);
      -webkit-box-shadow: 0px 0px 0px 1px transparent inset, none;
      box-shadow: 0px 0px 0px 1px transparent inset, none;
    }

  }
  .wlt.active.button{
    background-color: #C0C1C2;
    background-image: none;
    -webkit-box-shadow: 0px 0px 0px 1px transparent inset;
    box-shadow: 0px 0px 0px 1px transparent inset;
    color: rgba(0, 0, 0, 0.95);
  }


</style>
