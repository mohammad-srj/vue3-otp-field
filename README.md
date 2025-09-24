# Vue-Vite 3 OTP Input Field

Customizable OTP input field component for Vue 3 Vite.

> Recommended to use with Vue Vite. Because Vue(without Vite) does not accept the emit funcitons as node package.

## Preview

![Gifphy](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOTNlaHhmeXBvMXI1ZG5wc3RobmNmNDN6cnEyZW9kNzRjdG1jamV5NSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/VLcjJZfpPEHEhSbw0k/giphy.gif)

## Demo

[Demo link](https://stackblitz.com/edit/vitejs-vite-6bb2ro?file=src%2FApp.vue)

## Installation

To install:

```sh
npm i vue3-otp-input-field
```

OR

```sh
yarn add vue3-otp-input-field
```

OR

Without Build Tools

```sh
<script src="https://unpkg.com/vue3-otp-input-field"></script>
```

## Usage

In your desired component add the OTP component with required props

```ts
<script setup>
import { ref } from "vue";
import { OTP } from "vue3-otp-input-field";

function logOtpValue(val = []) {
  code.value = val;
}
const code = ref([]);
const fieldSize = ref(6);
const autoFocus = ref(true)

function handleSubmit() {
  console.log(code.value);
}
</script>

<template>
  <OTP
    size="medium"
    :fields="fieldSize"
    inputstyle="width: 80px; height: 50px; font-size: 40px; margin: 3px; border-radius: 5px;"
    type="mix"
    :auto-focus = autoFocus
    className="example-class-name"
    @OTPValueChanged="logOtpValue"
  />

  <div class="card">
    <button type="button" @click="handleSubmit">Submit</button>
  </div>
  <h1>{{ code }}</h1>
</template>

<style scoped></style>

```

## Props parameters

| Prop/Attribute     | Type       | Description                                                                    |
|--------------------|------------|--------------------------------------------------------------------------------|
| `size`             | `string`   | Size of the OTP component (`"small"`, `"medium"`, `"large"`)                   |
| `:fields`          | `number`   | Specify the number of input box                                                |
| `inputstyle`       | `string`   | Styles applied to each input field (CSS inline styles)                         |
| `type`             | `string`   | Type of OTP (`"number"`, `"mix"`)                                              |
| `className`        | `string`   | Additional class name(s) for styling or customization                          |
| `auto-focus`       | `boolean`  | Auto focuses input on initial page load.                                       |
| `@OTPValueChanged` | `function` | Event handler for OTP value change (Vue.js event binding). Its a Emit function |

## Contribute

Contributions are always welcome!
