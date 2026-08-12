<script setup lang="js">
import {
  Bell,
  EllipsisVertical,
  Menu,
  Mic,
  Search,
  SearchX,
  UserCircle,
} from "@lucide/vue";
import AppLogo from "../AppLogo.vue";
import UserMenu from "../../ui/UserMenu.vue";
</script>
<template>
  <!-- Desktop screen menu -->
  <nav
    class="hidden md:flex items-center py-2 px-4 shadow-xs w-full fixed z-20 bg-gray-50 top-0 overflow-x-hidden"
  >
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

  <!-- Mobile screen menu -->
  <nav
    class="flex items-center justify-between sticky top-0 z-20 bg-gray-50 shadow-xs py-2 px-4 md:hidden"
  >
    <AppLogo />

    <div class="flex items-center gap-4">
      <Bell size="20" />
      <Search size="20" />
    </div>
  </nav>
</template>
