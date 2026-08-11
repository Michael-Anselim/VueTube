<script setup lang="js">
import {
  Flag,
  Gamepad2,
  Home,
  Medal,
  Music2,
  RotateCcwClock,
  Trophy,
  TvMinimalPlay,
  UserCircle,
  Video,
} from "@lucide/vue";
import Separator from "../ui/Separator.vue";
import UserMenu from "../ui/UserMenu.vue";

const menuItems = [
  { icon: Home, label: "Home" },
  { icon: Video, label: "Shorts" },
  { icon: TvMinimalPlay, label: "Subscriptions" },
  { icon: UserCircle, label: "You" },
  { icon: RotateCcwClock, label: "History" },
];

const exploreItems = [
  { icon: Music2, label: "Music" },
  { icon: Gamepad2, label: "Gaming" },
  { icon: TvMinimalPlay, label: "Sports" },
  { icon: UserCircle, label: "Memberships" },
];

const moreItems = [
  { icon: Music2, label: "Try Premium for $0" },
  { icon: Gamepad2, label: "VueTube Music" },
  { icon: Trophy, label: "VueTube kids" },
];
</script>

<template>
  <aside class="rid grid-cols-1 space-y-2 max-w-48 py-8">
    <div class="grid grid-cols-1 space-y-2">
      <!-- Basic links -->
      <div
        v-for="item in menuItems"
        :key="item.label"
        class="flex items-center flex-col xl:flex-row gap-2 hover:bg-gray-200/60 py-1.5 rounded-full"
      >
        <component :is="item.icon" size="20" />
        <span class="text-sm">{{ item.label }}</span>
      </div>
      <Separator />
    </div>
    <!-- Sign in div -->
    <div class="space-y-2">
      <p class="text-sm">Sign in to like videos, comment, and subscribe.</p>
      <UserMenu />
      <Separator />
    </div>
    <!-- Explore div -->
    <div>
      <h1 class="text-lg mb-3 font-semibold">Explore</h1>
      <div class="grid grid-cols-1 space-y-2">
        <div
          v-for="item in exploreItems"
          :key="item.label"
          class="flex items-center gap-2 hover:bg-gray-200/60 py-1.5 rounded-full"
        >
          <component :is="item.icon" size="20" />
          <span class="text-sm">{{ item.label }}</span>
        </div>
        <Separator />
      </div>
    </div>
    <!-- More from youtube div -->
    <div>
      <h1 class="text-lg mb-3 font-semibold">More from VueTube</h1>
      <div class="grid grid-cols-1 space-y-2">
        <div
          v-for="item in moreItems"
          :key="item.label"
          class="flex items-center gap-2 hover:bg-gray-200/60 py-1.5 rounded-full"
        >
          <component :is="item.icon" size="20" />
          <span class="text-sm">{{ item.label }}</span>
        </div>
        <Separator />
      </div>
    </div>
    <!-- Report div -->
    <div>
      <div class="flex gap-2 py-2">
        <Flag />
        <span class="text-sm">Report history</span>
      </div>
      <Separator />
    </div>
    <!-- Copyright div -->
    <div class="text-sm flex flex-col gap-2">
      <p>This app is developed for learning purposes only</p>
      <P> No commercial or any unrelated uses are allowed </P>
      <P class="text-xs text-gray-400"> @2026 VueTube LLC</P>
    </div>
  </aside>
</template>
