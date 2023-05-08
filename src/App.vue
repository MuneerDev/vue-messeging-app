<template>
  <div class="mt-5">
    <messegingApp :converations="converations"></messegingApp>
  </div>
</template>

<script setup>
import messegingApp from "./components/messegingApp.vue";
const converations = [
  {
    name: "Haider",
    lastMessage:
      "Yeah, I watched the new Marvel movie last weekend. It was pretty good!",
    messeges: [
      { messege: "hello friend", outgoing: false },
      { messege: "Hey my friend!", outgoing: true },
      { messege: "how are are doing", outgoing: false },
      { messege: "doing pretty well!", outgoing: true },
      { messege: "Have you seen any good movies lately?", outgoing: true },
      {
        messege:
          "Yeah, I watched the new Marvel movie last weekend. It was pretty good!",
        outgoing: false,
      },
      {
        messege:
          "That's cool. I haven't seen it yet. I've been too busy with work.",
        outgoing: true,
      },
      {
        messege: "Yeah, I know what you mean. It's been crazy at my job too.",
        outgoing: false,
      },
    ],
  },
  {
    name: "Azez",
    lastMessage: "Perfect. I've been wanting to try that place out.",
    messeges: [
      { messege: "hey my dear friend", outgoing: false },
      { messege: "Hey!", outgoing: true },
      { messege: "what you been up to", outgoing: true },
      { messege: "nothing much", outgoing: false },
      {
        messege: "Do you want to grab lunch sometime this week?",
        outgoing: true,
      },
      {
        messege: "Sure, that sounds great. How about Wednesday?",
        outgoing: false,
      },
      {
        messege:
          "Wednesday works for me. How about we meet at the new Italian place downtown?",
        outgoing: true,
      },
      {
        messege: "Perfect. I've been wanting to try that place out.",
        outgoing: false,
      },
    ],
  },
  {
    name: "Muneer",
    lastMessage: "Definitely. Let me send you a list of my favorites.",
    messeges: [
      { messege: "wassup", outgoing: true },
      { messege: "wassup", outgoing: false },
      { messege: "did you play that game!", outgoing: true },
      { messege: "hell yah i did", outgoing: false },
      { messege: "Which game did you play?", outgoing: false },
      {
        messege:
          "I played the new racing game that just came out. It's really fun!",
        outgoing: true,
      },
      {
        messege:
          "Oh, cool. I haven't played that one yet. I've been playing a lot of RPGs lately.",
        outgoing: false,
      },
      {
        messege:
          "I've been meaning to try out more RPGs. Do you have any recommendations?",
        outgoing: true,
      },
      {
        messege: "Definitely. Let me send you a list of my favorites.",
        outgoing: false,
      },
    ],
  },
  {
    name: "Sara",
    lastMessage: "doing pretty well!",
    messeges: [
      { messege: "hello friend", outgoing: false },
      { messege: "Hey my friend!", outgoing: true },
      { messege: "how are are doing", outgoing: false },
      { messege: "doing pretty well!", outgoing: true },
      { messege: "Want to catch up over coffee sometime?", outgoing: true },
      { messege: "Sure, that sounds good!", outgoing: false },
      { messege: "How about this weekend?", outgoing: true },
      { messege: "I'm free on Sunday afternoon.", outgoing: false },
      {
        messege: "Sounds good, let's meet at the cafe on Main Street at 2 pm.",
        outgoing: true,
      },
      { messege: "Great, see you then!", outgoing: false },
    ],
  },
];
</script>
