<script setup>
defineProps({
  imagePath: String
})

</script>

<template>
  <img :src="imagePath" class="profile" alt="profile" />
</template>