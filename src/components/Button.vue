<template>
  <div style="text-align: center;margin-top: 100px">
    <button class="wlt button">按钮</button>
    <button class="wlt active button">按钮</button>
    <button class="wlt primary button">按钮</button>
    <button class="wlt active primary button">按钮</button>
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
  /*******************************
              primary
  *******************************/
  /* Standard */
  .wlt.primary.button {
    background-color: #2185D0;
    color: #FFFFFF;
    text-shadow: none;
    background-image: none;
    -webkit-box-shadow: 0px 0em 0px 0px rgba(34, 36, 38, 0.15) inset;
    box-shadow: 0px 0em 0px 0px rgba(34, 36, 38, 0.15) inset;
    &:hover {
      background-color: #1678c2;
      color: #FFFFFF;
      text-shadow: none;
    }
    &:focus {
      background-color: #0d71bb;
      color: #FFFFFF;
      text-shadow: none;
    }
    &:active {
      background-color: #1a69a4;
      color: #FFFFFF;
      text-shadow: none;
    }
    .active.button{
      &:active {
        background-color: #1279c6;
        color: #FFFFFF;
        text-shadow: none;
      }
    }
  }
  .wlt.primary.active.button{
    background-color: #1279c6;
    color: #FFFFFF;
    text-shadow: none;
  }
  .wlt.primary.buttons{
    .button{
      &:hover{
        background-color: #1678c2;
        color: #FFFFFF;
        text-shadow: none;
      }
      &:focus{
        background-color: #0d71bb;
        color: #FFFFFF;
        text-shadow: none;
      }
      &:active{
        background-color: #1a69a4;
        color: #FFFFFF;
        text-shadow: none;
      }
    }
    .active.button{
      background-color: #1279c6;
      color: #FFFFFF;
      text-shadow: none;
      &:active{
        background-color: #1279c6;
        color: #FFFFFF;
        text-shadow: none;
      }
    }
  }
  /* Basic */
  .wlt.basic.primary.button{
    -webkit-box-shadow: 0px 0px 0px 1px #2185D0 inset !important;
    box-shadow: 0px 0px 0px 1px #2185D0 inset !important;
    color: #2185D0 !important;
    &:hover{
      background: transparent !important;
      -webkit-box-shadow: 0px 0px 0px 1px #1678c2 inset !important;
      box-shadow: 0px 0px 0px 1px #1678c2 inset !important;
      color: #1678c2 !important;
    }
    &:focus{
      background: transparent !important;
      -webkit-box-shadow: 0px 0px 0px 1px #0d71bb inset !important;
      box-shadow: 0px 0px 0px 1px #0d71bb inset !important;
      color: #1678c2 !important;
    }
    &:active{
      -webkit-box-shadow: 0px 0px 0px 1px #1a69a4 inset !important;
      box-shadow: 0px 0px 0px 1px #1a69a4 inset !important;
      color: #1a69a4 !important;
    }
  }
  .wlt.basic.primary.buttons{
    .button{
      -webkit-box-shadow: 0px 0px 0px 1px #2185D0 inset !important;
      box-shadow: 0px 0px 0px 1px #2185D0 inset !important;
      color: #2185D0 !important;
      &:hover {
        background: transparent !important;
        -webkit-box-shadow: 0px 0px 0px 1px #1678c2 inset !important;
        box-shadow: 0px 0px 0px 1px #1678c2 inset !important;
        color: #1678c2 !important;
      }
      &:focus{
        background: transparent !important;
        -webkit-box-shadow: 0px 0px 0px 1px #0d71bb inset !important;
        box-shadow: 0px 0px 0px 1px #0d71bb inset !important;
        color: #1678c2 !important;
      }
      &:active {
        -webkit-box-shadow: 0px 0px 0px 1px #1a69a4 inset !important;
        box-shadow: 0px 0px 0px 1px #1a69a4 inset !important;
        color: #1a69a4 !important;
      }
    }
    .active.button{
      background: transparent !important;
      -webkit-box-shadow: 0px 0px 0px 1px #1279c6 inset !important;
      box-shadow: 0px 0px 0px 1px #1279c6 inset !important;
      color: #1a69a4 !important;
    }
  }
  .wlt.basic.primary.active.button {
    background: transparent !important;
    -webkit-box-shadow: 0px 0px 0px 1px #1279c6 inset !important;
    box-shadow: 0px 0px 0px 1px #1279c6 inset !important;
    color: #1a69a4 !important;
  }
  .wlt.buttons:not(.vertical) > .basic.primary.button:not(:first-child) {
    margin-left: -1px;
  }




  /* Inverted */
  .wlt.inverted.primary.buttons .button,
  .wlt.inverted.primary.button {
    background-color: transparent;
    -webkit-box-shadow: 0px 0px 0px 2px #54C8FF inset !important;
    box-shadow: 0px 0px 0px 2px #54C8FF inset !important;
    color: #54C8FF;
  }
  .wlt.inverted.primary.buttons .button:hover,
  .wlt.inverted.primary.button:hover,
  .wlt.inverted.primary.buttons .button:focus,
  .wlt.inverted.primary.button:focus,
  .wlt.inverted.primary.buttons .button.active,
  .wlt.inverted.primary.button.active,
  .wlt.inverted.primary.buttons .button:active,
  .wlt.inverted.primary.button:active {
    -webkit-box-shadow: none !important;
    box-shadow: none !important;
    color: #FFFFFF;
  }
  .wlt.inverted.primary.buttons .button:hover,
  .wlt.inverted.primary.button:hover {
    background-color: #3ac0ff;
  }
  .wlt.inverted.primary.buttons .button:focus,
  .wlt.inverted.primary.button:focus {
    background-color: #2bbbff;
  }
  .wlt.inverted.primary.buttons .active.button,
  .wlt.inverted.primary.active.button {
    background-color: #3ac0ff;
  }
  .wlt.inverted.primary.buttons .button:active,
  .wlt.inverted.primary.button:active {
    background-color: #21b8ff;
  }

  /* Inverted Basic */
  .wlt.inverted.primary.basic.buttons .button,
  .wlt.inverted.primary.buttons .basic.button,
  .wlt.inverted.primary.basic.button {
    background-color: transparent;
    -webkit-box-shadow: 0px 0px 0px 2px rgba(255, 255, 255, 0.5) inset !important;
    box-shadow: 0px 0px 0px 2px rgba(255, 255, 255, 0.5) inset !important;
    color: #FFFFFF !important;
  }
  .wlt.inverted.primary.basic.buttons .button:hover,
  .wlt.inverted.primary.buttons .basic.button:hover,
  .wlt.inverted.primary.basic.button:hover {
    -webkit-box-shadow: 0px 0px 0px 2px #3ac0ff inset !important;
    box-shadow: 0px 0px 0px 2px #3ac0ff inset !important;
    color: #54C8FF !important;
  }
  .wlt.inverted.primary.basic.buttons .button:focus,
  .wlt.inverted.primary.basic.buttons .button:focus,
  .wlt.inverted.primary.basic.button:focus {
    -webkit-box-shadow: 0px 0px 0px 2px #2bbbff inset !important;
    box-shadow: 0px 0px 0px 2px #2bbbff inset !important;
    color: #54C8FF !important;
  }
  .wlt.inverted.primary.basic.buttons .active.button,
  .wlt.inverted.primary.buttons .basic.active.button,
  .wlt.inverted.primary.basic.active.button {
    -webkit-box-shadow: 0px 0px 0px 2px #3ac0ff inset !important;
    box-shadow: 0px 0px 0px 2px #3ac0ff inset !important;
    color: #54C8FF !important;
  }
  .wlt.inverted.primary.basic.buttons .button:active,
  .wlt.inverted.primary.buttons .basic.button:active,
  .wlt.inverted.primary.basic.button:active {
    -webkit-box-shadow: 0px 0px 0px 2px #21b8ff inset !important;
    box-shadow: 0px 0px 0px 2px #21b8ff inset !important;
    color: #54C8FF !important;
  }



</style>
