<template>
    <div class="kaya">
      <h2>Kamu ingin kaya ? Klik dibawah ini</h2>
      <Enmit2 @message-from-grandchild="ehe" />
      <slot name="additionalContent"></slot>
    </div>
  </template>
  
  <script>
  import Enmit2 from './Emit2.vue';
  
  export default {
    components: {
      Enmit2,
    },
    methods: {
      ehe(payload) {
        this.$emit('message-from-child', payload);
      },
    },
  };
  </script>
  
  <style scoped>
  .kaya {
    padding: 15px;
    background-color: #e3e3e3;
    border: 1px solid #ccc;
    border-radius: 5px;
    margin-top: 10px;
  }
  </style>
  