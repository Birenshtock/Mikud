<template>
  <appHeader></appHeader>

  <RouterView />

  <!-- <appFooter></appFooter> -->
</template>

<script>
import { RouterLink, RouterView } from 'vue-router'
import appHeader from './components/header.vue'
import appFooter from './components/footer.vue'

export default {
  components: {
    appHeader,
    appFooter,
  },
  data: () => {
    return {}
  },
  methods: {},
  computed: {},
}
</script>
<style></style>
