<script lang="ts" setup>
import {computed, ref} from 'vue';

const msg = ref('Hello Wolrd!');
const message = "I'm the originalmessage";
const myBool = ref(true);

const reversedMessage = computed(() => {
  return message.split('').reverse().join('');
});

const toggleText = () => {
  myBool.value = !myBool.value;
};
</script>


<template>
  <div class="about">
    <h1><u>This is a code page</u></h1>
    <h2>{{ msg }}</h2>
    <input type="text" v-model="msg">
    <br>
    <p class="click-p" @click="toggleText">{{myBool ? message : reversedMessage }}</p>
  </div>
</template>


<style>

.click-p {
  cursor: pointer;
}
</style>



