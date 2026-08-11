<script setup lang="js">
import AppLayout from "../components/AppLayout.vue";
import logo from "../assets/vue.svg";
import { CircleCheck, EllipsisVertical } from "@lucide/vue";

const shortcutsLabel = [
  "All",
  "APIs",
  "Codding",
  "Vuejs",
  "Frontend",
  "Tailwind",
  "Laravel",
  "FastApPI",
  "Database",
  "Next.js",
  "React",
  "PHP",
  "Music",
];

const videoData = [
  {
    title: "Taylor Otwell on how he tackles large projects",
    image: logo,
    user: "MIchael anselim",
  },
  {
    title: "Taylor Otwell on how he tackles large projects",
    image: logo,
    user: "MIchael anselim",
  },
  {
    title: "Taylor Otwell on how he tackles large projects",
    image: logo,
    user: "MIchael anselim",
  },
  {
    title: "Taylor Otwell on how he tackles large projects",
    image: logo,
    user: "MIchael anselim",
  },
  {
    title: "Taylor Otwell on how he tackles large projects",
    image: logo,
    user: "MIchael anselim",
  },
  {
    title: "Taylor Otwell on how he tackles large projects",
    image: logo,
    user: "MIchael anselim",
  },
  {
    title: "Taylor Otwell on how he tackles large projects",
    image: logo,
    user: "MIchael anselim",
  },
  {
    title: "Taylor Otwell on how he tackles large projects",
    image: logo,
    user: "MIchael anselim",
  },
  {
    title: "Taylor Otwell on how he tackles large projects",
    image: logo,
    user: "MIchael anselim",
  },
  {
    title: "Taylor Otwell on how he tackles large projects",
    image: logo,
    user: "MIchael anselim",
  },
  {
    title: "Taylor Otwell on how he tackles large projects",
    image: logo,
    user: "MIchael anselim",
  },
  {
    title: "Taylor Otwell on how he tackles large projects",
    image: logo,
    user: "MIchael anselim",
  },
];
</script>
<template>
  <app-layout>
    <section>
      <div class="flex gap-2 py-4">
        <button
          v-for="label in shortcutsLabel"
          class="bg-gray-200/70 rounded-2xl h-fit py-1 px-3"
        >
          {{ label }}
        </button>
      </div>
      <div class="flex flex-wrap gap-8 justify-around">
        <!-- Video card -->
        <article
          class="max-w-md px-4 py-8 rounded-2xl shadow-xs hover:bg-green-50/50 hover:shadow-md"
          v-for="data in videoData"
        >
          <img
            :src="data.image"
            alt="Video-image"
            class="w-full h-48 m-auto rounded-lg shadow-xxs mb-4"
          />
          <div class="flex items-center gap-4">
            <img
              :src="data.image"
              alt="ProfilePicture"
              class="border border-blue-200 rounded-full p-2"
            />
            <!-- Video details -->
            <div class="space-y-1">
              <h2 class="text-md font-semibold">{{ data.title }}....</h2>
              <div class="flex gap-1 items-center text-sm text-gray-400">
                <p>{{ data.user }}</p>
                <circle-check
                  size="16"
                  class="bg-gray-500 rounded-full text-gray-200"
                />
              </div>
              <p class="text-gray-400 text-sm">
                20K views . <span>! day ago</span>
              </p>
            </div>
            <ellipsis-vertical size="20" />
          </div>
        </article>
      </div>
    </section>
  </app-layout>
</template>
