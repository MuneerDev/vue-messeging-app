<template>
  <ul class="grid p-5 gap-10 text-white">
    <li
      v-for="(messege, index) in converations"
      :key="index"
      :class="`${messege.outgoing ? reciver : sender}`">
      {{ messege.messege }}
    </li>
  </ul>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  converations: {
    type: [Array],
    required: true,
  },
});

const reciver = "bg-blue-500 rounded-lg w-fit px-5 py-3 received relative";
const sender =
  "bg-green-500 rounded-lg w-fit px-5 py-3 sent relative justify-self-end";
console.log(props.converations[0].messege);
</script>
