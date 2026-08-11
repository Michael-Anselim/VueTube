<script setup lang="js">
import { EllipsisVertical, Menu, Mic, Search, UserCircle } from "@lucide/vue";
import AppLogo from "../AppLogo.vue";
import UserMenu from "../../ui/UserMenu.vue";
</script>
<template>
  <nav class="flex items-center py-1 px-2 shadow-xs mt-2">
    <!-- Menu  button and Logo -->
    <div class="flex items-center gap-4 w-[25%]">
      <Menu size="20" />
      <AppLogo />
    </div>
    <!-- Search panel -->
    <div class="flex items-center gap-4 w-[50%]">
      <div class="flex items-center w-[80%]">
        <input
          type="search"
          name=""
          id=""
          placeholder="Search..."
          class="py-2 px-4 border border-gray-200 rounded-l-full w-full"
        />
        <button
          class="bg-gray-200/60 py-2 text-lg px-6 rounded-r-3xl font-bold"
        >
          <Search size="24" />
        </button>
      </div>
      <div class="rounded-full p-2 bg-gray-200/60">
        <Mic />
      </div>
    </div>
    <!-- Dots and sign in/out menus -->
    <div class="flex items-center gap-4 w-[25%] justify-end">
      <div class="p-1">
        <EllipsisVertical size="20" />
      </div>
      <UserMenu />
    </div>
  </nav>
</template>
