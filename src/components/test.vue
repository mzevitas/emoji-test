<template>
<div id="init">hom

    <input type="text">
    <div class="selector-btn">
        <p id="click" v-on:click="isHidden = !isHidden">touch</p>

        <p >testeet</p>
      <picker  sheetURL='…' onClick={this.addEmoji} v-if="!isHidden" set="emojione"/>
    </div>

</div>
</template>

<style>
  .emoji-mart-bar {
    display: none;
  }
  .show {
    display: block;
  }
  .hide {
    display: none;
  }
</style>



<script>
import {Picker} from 'emoji-mart-vue'


export default {
     name: 'HelloWorld',

  components: {
    Picker
  },

  data () {
    return {
       isHidden: true
    }
  }


  }
</script>

