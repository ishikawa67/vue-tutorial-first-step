<template>
  <div class="hello">
    <h1>{{ message }}</h1>
    <p>{{ description }}</p>
    <button @click="changeMessage">Click Me</button>
  </div>
</template>

<script setup lang="ts">
// Propsの型定義
interface Props {
  description: string;
}

// Propsを定義
const props = defineProps<Props>();

// リアクティブな状態の定義
import { ref } from 'vue';
const message = ref<string>('Hello, Vue 3 with <script setup> and TypeScript!');

// メソッドの定義
let changeFlag = true;
const changeMessage = (): void => {
  if (changeFlag) {
    message.value = 'You clicked the button! firstTime or odd';
    changeFlag = !changeFlag;
  } else {
    message.value = 'You clicked the button! even times';
    changeFlag = !changeFlag;
  }
};
</script>

<style scoped>
.hello {
  text-align: center;
  color: #333;
}

button {
  background-color: #42b983;
  color: white;
  border: none;
  padding: 10px;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #369b73;
}
</style>
