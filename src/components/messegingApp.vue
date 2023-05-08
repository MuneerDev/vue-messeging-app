<template>
  <div
    class="container mx-auto max-w-[90%] relative bg-gray-200 min-h-[85vh] rounded overflow-y-auto">
    <ul class="grid gap-5 rounded mt-5 p-5">
      <li
        class="hover:bg-indigo-300 rounded p-3 pl-5 cursor-pointer duration-300 flex items-center gap-8 border-b border-gray-300 last:shadow-none last:border-b-0"
        v-for="(converation, index) in converations"
        :key="index"
        @click="SelectConverstion(index)">
        <img :src="link + index" alt="person" class="rounded-full w-20 h-20" />
        <div class="font-bold text-2xl">
          <p>{{ converation.name }}</p>
          <p class="font-normal text-gray-500 text-lg truncate w-[15ch]">
            {{ converation.lastMessage }}
          </p>
        </div>
      </li>
    </ul>
    <div :class="`${styleMesseges} ${dropDownNoActive}`">
      <button
        @click="SelectConverstion"
        class="px-5 pt-3 pb-4 w-fit bg-indigo-500 rounded-lg text-white font-bold text-3xl">
        &lt;
      </button>
      <MessegesContent
        :converations="
          props.converations[converationIndex].messeges
        "></MessegesContent>
    </div>
  </div>
</template>

<script setup>
import { defineProps, ref } from "vue";
import MessegesContent from "./MessegesContent.vue";
const props = defineProps({
  converations: {
    type: [Array],
    required: true,
  },
});

const converationIndex = ref(0);

const styleMesseges =
  "w-full bg-gray-300 absolute min-h-[90vh] rounded p-10 duration-300 top-[-150%]";

const selectedMessege = ref(false);

const dropDownNoActive = ref("");

const SelectConverstion = (index) => {
  selectedMessege.value = !selectedMessege.value;
  if (selectedMessege.value) {
    dropDownNoActive.value = "dropDown";
    converationIndex.value = index;
  } else {
    dropDownNoActive.value = "";
  }
};

const link = `https://picsum.photos/100/100?random=`;
</script>
