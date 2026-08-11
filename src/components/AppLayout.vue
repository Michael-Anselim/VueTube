<script setup lang="js">
import {
  Flag,
  Gamepad2,
  Home,
  Medal,
  Music,
  Music2,
  RotateCcwClock,
  Trophy,
  TvMinimalPlay,
  UserCircle,
  Video,
} from "@lucide/vue";
import NavBar from "./partials/home/NavBar.vue";
import Separator from "./ui/Separator.vue";
import UserMenu from "./ui/UserMenu.vue";
import AppSideBar from "./partials/AppSideBar.vue";
</script>
<template>
  <NavBar />
  <main class="flex h-screen gap-8">
    <AppSideBar />
    <slot></slot>
  </main>
</template>
