<template>
  <div>
    <messegingApp :converations="converations"></messegingApp>
  </div>
</template>

<script setup>
import messegingApp from "./components/messegingApp.vue";
const converations = [
  {
    name: "Haider",
    lastMessage: "Hello World",
    messeges: [
      { messege: "hello friend", outgoing: false },
      { messege: "Hey my friend!", outgoing: true },
      { messege: "how are are doing", outgoing: false },
      { messege: "doing pretty well!", outgoing: true },
    ],
  },
  {
    name: "Azez",
    lastMessage: "Hello World",
    messeges: [
      { messege: "hey my dear friend", outgoing: false },
      { messege: "Hey!", outgoing: true },
      { messege: "what you been up to", outgoing: true },
      { messege: "nothing much", outgoing: false },
    ],
  },
  {
    name: "Muneer",
    lastMessage: "Hello World",
    messeges: [
      { messege: "wassup", outgoing: true },
      { messege: "wassup", outgoing: false },
      { messege: "did you play that game!", outgoing: true },
      { messege: "hell yah i did", outgoing: false },
    ],
  },
];
</script>
