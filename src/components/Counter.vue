<template>
  <div class="rounded border md:shadow">
    <div class="px-4 py-4 text-center justify-items-center m-8">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="h-40 w-40 mx-auto text-primary"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M9 3v2m6-2v2M9 19v2m6-2v2M5 9H3m2 6H3m18-6h-2m2 6h-2M7 19h10a2 2 0 002-2V7a2 2 0 00-2-2H7a2 2 0 00-2 2v10a2 2 0 002 2zM9 9h6v6H9V9z"
        />
      </svg>

      <div class="text-xl text-gray-800">
        {{ count }}
      </div>
      <div class="text-lg text-gray-800">Article counted</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
};
</script>

<style>
</style>