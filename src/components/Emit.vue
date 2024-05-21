<template>
  <div class="container">
    <h1>Cara cepat kaya</h1>
    <p>{{ message }}</p>
    <Slot @message-from-child="handleMessageFromChild">
      <template v-slot:additionalContent>
        <p>© Randy Ivando 2024 </p>
      </template>
    </Slot>
  </div>
</template>

<script>
import Slot from './Slot.vue';

export default {
  components: {
    Slot,
  },
  data() {
    return {
      message: '',
    };
  },
  methods: {
    handleMessageFromChild(payload) {
      this.message = payload;
    },
  },
};
</script>

<style scoped>
.container {
  background: #fbfbfb;
  border-radius: 8px;
  box-shadow: 1px 2px 8px rgba(0, 0, 0, 0.65);
  height: 410px;
  margin: 6rem auto 8.1rem auto;
  width: 55%;
}
</style>