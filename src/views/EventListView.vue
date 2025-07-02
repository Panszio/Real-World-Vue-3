
<script setup>
import EventCard from '@/components/EventCard.vue'
import axios from 'axios'
import { onMounted, ref } from 'vue'

const events = ref(null)
  
  onMounted(() => {
    axios.get(' https://my-json-server.typicode.com/Panszio/Real-Wolrd_Vue-3/')
  })
</script>

<template>
  <h1>Events For Good</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
