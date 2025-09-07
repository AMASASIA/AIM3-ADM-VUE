<template>
  <div class="container">
    <div class="header">
      <div style="display:flex; align-items:center; gap:12px;">
        <strong>0DAO · Osaka Place Making DAO</strong>
        <span class="pill">OKE CARD</span>
      </div>
      <div style="display:flex; gap:10px; align-items:center;">
        <RouterLink to="/dashboard" class="muted">Dashboard</RouterLink>
        <RouterLink to="/proposal" class="muted">Proposal</RouterLink>
        <RouterLink to="/treasury" class="muted">Treasury</RouterLink>
        <RouterLink to="/voting" class="muted">Voting</RouterLink>
        <button class="btn ghost" @click="store.toggleTheme()">Toggle {{ store.theme==='dark'?'Light':'Dark' }}</button>
        <button v-if="store.user" class="btn ghost" @click="store.logout()">Logout</button>
      </div>
    </div>
    <RouterView />
  </div>
</template>

<script setup lang="ts">
import { RouterView, RouterLink } from 'vue-router'
import { useAppStore } from './store/app'
const store = useAppStore()
</script>
