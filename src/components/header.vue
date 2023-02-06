<template>
  <header class="header">
    <nav class="main-layout">
      <div></div>

      <RouterLink class="header-item" to="/contactUs">
        <div>עברית</div>
      </RouterLink>
      <RouterLink class="header-item" to="/contactUs">
        <div>אנגלית</div>
      </RouterLink>
      <RouterLink class="header-item" to="/contactUs">
        <div>סטודנטים</div>
      </RouterLink>
      <RouterLink class="header-item" to="/contactUs">
        <div>צור קשר</div>
      </RouterLink>
      <RouterLink class="header-item" to="/">
        <div>אודות</div>
      </RouterLink>
      <RouterLink class="header-item" to="/">
        <img class="logo" src="../../src/styles/imgs/logo.png" alt="" />
      </RouterLink>
    </nav>
  </header>
</template>
<script>
export default {
  components: {},
  data: () => {
    return {}
  },
  methods: {},
  computed: {},
}
</script>
