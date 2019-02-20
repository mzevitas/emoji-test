<template>
  <div class="home-page">

    <h1>Text Area</h1>
    <textarea-emoji-picker
      v-model="text"
    />

    <h1>Input</h1>
    <input-emoji-picker
    v-model="input"/>
  </div>
</template>




<script>
import TextareaEmojiPicker from '../components/TextareaEmojiPicker.vue'
import InputEmojiPicker from '../components/InputEmojiPicker.vue'



export default {

components: { TextareaEmojiPicker, InputEmojiPicker },
  data () {
    return {
      text: '',
      input: ''
    }
  }
}

</script>

<style scoped>
  h1 {
    font-size: 20px;
  }
</style>

