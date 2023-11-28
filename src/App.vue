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
  </div>
</template>

<script setup lang="ts">
import OTP from "./components/OTP.vue";

function logOtpValue(val = []) {
  console.log(val);
}
</script>
<style lang="scss"></style>
