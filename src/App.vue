<template>
  <div>
    <h1>Vue 3 OTP Input Field Package - DEMO</h1>
    <OTP
      size="large"
      :fields="6"
      inputstyle="width: 80px; height: 50px; font-size: 40px; margin: 3px; border-radius: 5px;"
      type="mix"
      className="mt-5"
      @OTPValueChanged="logOtpValue"
    />
    <p>
      OTP Value: <span v-for="n in otpValue" :key="n">{{ n }}</span>
    </p>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import OTP from "./components/OTP.vue";
const otpValue = ref([]);

function logOtpValue(val = []) {
  console.log(val);
  otpValue.value = val;
}
</script>
<style lang="scss"></style>
