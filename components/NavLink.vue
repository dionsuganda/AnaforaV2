<template>
  <li class="w-full">
    <a
      class="md:px-4 py-2 text-base font-semibold bg-transparent rounded-lg text-[#ffffff] hover:text-gray-900 focus:outline-none focus:shadow-outline"
      :href="url"
    >
      {{ name }}
    </a>
  </li>
</template>
<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
    url: {
      type: String,
      required: true,
    },
  },
}
</script>
