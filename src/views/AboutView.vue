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
    <h2>-> <span  class="textBlue">{{ msg }}</span> &lt;-</h2>
    <input type="text" v-model="msg">
    <br>
    <div class="container_click-p"> 
      <span>Click on this text -></span>
      <p class="click-p textBlue" @click="toggleText">{{ myBool ? message : reversedMessage }}</p>
    </div>
    <div>
      <li>
        <a href="/more-code">Go to more Vue code</a>
      </li>
    </div>
  </div>
</template>


<style>

.container_click-p {
 display: flex;
 flex-direction: row;
 justify-content: center;
 align-items: center;
 gap: 18px;
}

.click-p {
  cursor: pointer;
  font-size: larger;
  font-weight: 600;
}

.textBlue {
  color: rgb(0, 0, 255);
}
</style>



