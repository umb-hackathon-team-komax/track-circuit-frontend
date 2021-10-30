<template>
  <div class="rounded border md:shadow">
    <div class="flex flex-wrap px-4 py-4 gap-4">
      <div class="mx-auto">
        <button
          class="
            bg-green-500
            hover:bg-green-700
            text-white
            font-bold
            py-4
            px-5
            rounded
          "
        >
          Start
        </button>
      </div>
      <div class="mx-auto">
        <button
          class="
            bg-red-500
            hover:bg-red-700
            text-white
            font-bold
            py-4
            px-6
            rounded
          "
        >
          Stop
        </button>
      </div>
      <div class="mx-auto">
        <button
          class="
            bg-blue-500
            hover:bg-blue-700
            text-white
            font-bold
            py-4
            px-6
            rounded
          "
        >
          Reset
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>