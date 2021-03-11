<template>
  <div class="chat-bubble-wrap" :class="{'gray':user}">
     <div class="chat-bubble">{{msg}}</div>
  </div>
</template>

<script>
export default {
  name: 'chatline',
  props: {
    msg: String,
  user:Boolean
  }
}
</script>

