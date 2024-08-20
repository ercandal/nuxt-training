<template>
    <div class="conteiner">
      <div class="d-flex justify-content-center">
        <nav >
      <ul class="pagination">
        <li class="page-item" :class="{ disabled: currentPage === 1 }">
          <NuxtLink class="page-link" :to="`/products/${currentPage - 1}`">Previous</NuxtLink>
        </li>
        <li class="page-item" v-for="page in totalPages" :key="page" :class="{ active: currentPage === page }">
          <NuxtLink class="page-link" :to="`/products/${page}`">{{ page }}</NuxtLink>
        </li>
        <li class="page-item" :class="{ disabled: currentPage === totalPages }">
          <NuxtLink class="page-link" :to="`/products/${currentPage + 1}`">Next</NuxtLink>
        </li>
      </ul>
    </nav>
      </div>
    </div>
  </template>
  
  <script setup>
  import { computed } from 'vue'
  
  const props = defineProps({
    total: Number,
    currentPage: Number,
  })
  
  const perPage = 6
  const totalPages = computed(() => Math.ceil(props.total / perPage))
  </script>
  