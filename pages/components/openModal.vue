<template>
    <div>
      <button
        @click="openModal"
        class="md:fixed absolute top-0 justify-end right-0 px-4 py-2 lg:mr-32 mr-4 md:mt-10 mt-4 text-white bg-blue-600 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-full"
        type="button"
      >
        i
      </button>
  
      <div
        v-if="isModalOpen"
        class="fixed inset-0 z-50 flex items-center justify-center bg-black bg-opacity-50"
      >
        <div
          ref="modalRef"
          class="relative lg:w-6/12 mx-4 lg:mx-0 bg-white rounded-lg shadow dark:bg-gray-700"
        >
          <div
            class="flex items-center justify-between p-4 md:p-5 border-b rounded-t dark:border-gray-600"
          >
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white">
              Eisen
            </h3>
            <button
              @click="closeModal"
              type="button"
              class="text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm w-8 h-8 ms-auto inline-flex justify-center items-center dark:hover:bg-gray-600 dark:hover:text-white"
            >
              <svg
                class="w-3 h-3"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 14 14"
              >
                <path
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6"
                />
              </svg>
              <span class="sr-only">Close modal</span>
            </button>
          </div>
  
          <div class="p-4 md:p-5 space-y-4">
            <slot></slot>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  import { ref, onMounted, onUnmounted } from "vue";
  import { onClickOutside } from "@vueuse/core";
  
  const isModalOpen = ref(false);
  
  const modalRef = ref(null);
  
  const openModal = () => {
    isModalOpen.value = true;
  };
  
  const closeModal = () => {
    isModalOpen.value = false;
  };
  
  onClickOutside(modalRef, closeModal);
  
  const handleKeyDown = (event: KeyboardEvent) => {
    if (event.key === "Escape" && isModalOpen.value) {
      closeModal();
    }
  };
  
  onMounted(() => {
    window.addEventListener("keydown", handleKeyDown);
  });
  
  onUnmounted(() => {
    window.removeEventListener("keydown", handleKeyDown);
  });
  </script>
  