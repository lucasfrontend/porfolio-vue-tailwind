<template>
  <div class="header">
    <Header />
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'

export default {
  name: 'HeaderView',
  components: {
      Header
  }
}
</script>
