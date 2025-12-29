<template>
  <q-layout view="hHh lpR fFf" class="bg-grey-1">
    <q-header class="bg-white text-primary shadow-2 backdrop-blur-md q-py-sm" height-hint="60">
      <q-toolbar class="q-px-lg">
        <q-btn flat no-caps no-wrap class="q-mr-sm" to="/">
          <q-icon name="dashboard" color="primary" size="28px" />
          <q-toolbar-title shrink class="text-weight-bold q-ml-sm text-h6 font-heading">
            CUSTO-MGT
          </q-toolbar-title>
        </q-btn>

        <q-space />

        <div class="q-gutter-sm row items-center no-wrap gt-sm">
          <q-btn flat no-caps label="Home" class="text-weight-medium" to="/" />
          <q-btn flat no-caps label="Features" class="text-weight-medium" />
          <q-btn flat no-caps label="Pricing" class="text-weight-medium" />
          <q-btn flat no-caps label="About" class="text-weight-medium" />
          <q-separator vertical inset class="q-mx-md" />
          <q-btn outline color="primary" label="Login" no-caps class="q-px-md" />
          <q-btn unelevated color="primary" label="Get Started" no-caps class="q-px-md shadow-1" />
        </div>

        <q-btn flat round dense icon="menu" class="lt-md" />
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
// Layout logic here if needed
</script>

<style lang="scss">
.font-heading {
  letter-spacing: -0.5px;
}
.backdrop-blur-md {
  backdrop-filter: blur(10px);
  background-color: rgba(255, 255, 255, 0.9);
}
.container {
  max-width: 1200px;
  margin: 0 auto;
}
.footer-link {
  color: inherit;
  text-decoration: none;
  transition: color 0.3s;
  &:hover {
    color: var(--q-primary);
  }
}
</style>
