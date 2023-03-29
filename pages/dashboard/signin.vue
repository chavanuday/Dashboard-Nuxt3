<template>
  <div class="flex items-center justify-center w-full">
    <!-- Modal toggle -->
    <button
      data-modal-target="authentication-modal"
      data-modal-toggle="authentication-modal"
      class="block text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
      @click="showModal = !showModal"
      type="button"
    >
      Toggle modal
    </button>
    <Signin v-show="showModal" @close-modal="showModal = false" />
  </div>
</template>

<script setup>
import Signin from "@/Components/Dashboard/Signin.vue";

let showModal = ref(false);
</script>

<style lang="scss" scoped></style>
