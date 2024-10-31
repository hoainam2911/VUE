<template>
  <div id="app">
    <h2>Transition Demo</h2>
    <TransitionDemo />

    <h2>TransitionGroup Demo</h2>
    <TransitionGroupDemo />

    <h2>KeepAlive Demo</h2>
    <KeepAliveDemo />

    <h2>Teleport Demo</h2>
    <TeleportDemo />

    <h2>Suspense Demo</h2>
    <SuspenseDemo />
  </div>
</template>

<script>
import TransitionDemo from './components/TransitionDemo.vue'
import TransitionGroupDemo from './components/TransitionGroupDemo.vue'
import KeepAliveDemo from './components/KeepAliveDemo.vue'
import TeleportDemo from './components/TeleportDemo.vue'
import SuspenseDemo from './components/SuspenseDemo.vue'

export default {
  components: {
    TransitionDemo,
    TransitionGroupDemo,
    KeepAliveDemo,
    TeleportDemo,
    SuspenseDemo,
  },
}
</script>

<style>
/* Style tùy chọn cho App.vue */
</style>
npm run serve
