<script setup lang="js">
import {
  Flag,
  Home,
  Plus,
  PlusCircle,
  TvMinimalPlay,
  Video,
} from "@lucide/vue";
import NavBar from "./partials/home/NavBar.vue";
import Separator from "./ui/Separator.vue";
import UserMenu from "./ui/UserMenu.vue";
import AppSideBar from "./partials/AppSideBar.vue";

const menuItems = [
  { icon: Home, label: "Home" },
  { icon: Video, label: "Shorts" },
  { icon: PlusCircle, label: "  " },
  { icon: TvMinimalPlay, label: "Subscriptions" },
];
</script>
<template>
  <NavBar />
  <!-- Desktop option -->
  <main class="hidden md:block h-screen gap-12">
    <AppSideBar />
    <slot></slot>
  </main>

  <!-- Mobile options -->
  <main class="block md:hidden px-2 pb-5 mb-4">
    <slot> </slot>
    <footer
      class="flex lg:hidden items-center bg-gray-50 w-full px-4 py-2 fixed bottom-0 justify-between mt-10"
    >
      <div
        v-for="item in menuItems"
        :key="item.label"
        class="flex font-semibold items-center flex-col xl:flex-row gap-1 py-0.5 hover:bg-gray-200/60 rounded-full"
      >
        <component :is="item.icon" size="20" class="text-gray-700" />
        <span class="text-xs">{{ item.label }}</span>
      </div>
    </footer>
  </main>
</template>
