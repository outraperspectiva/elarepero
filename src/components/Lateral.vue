<template>
  <v-app>
    <v-navigation-drawer
      expand-on-hover
      permanent
      rail
    >
      <v-list-item
        prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
        subtitle="sandra_a88@gmail.com"
        title="Sandra Adams"
      >
        <template #append>
          <v-btn
            icon="mdi-chevron-left"
            variant="text"
            @click.stop="rail = !rail"
          />
        </template>
      </v-list-item>

      <v-divider />

      <v-list density="compact" nav>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          :prepend-icon="item.icon"
          :title="item.title"
          :to="item.to"
        />
      </v-list>
    </v-navigation-drawer>

    <router-view />
  </v-app>
</template>

<script lang="ts" setup>
  import { ref } from 'vue'

  const drawer = ref(true)
  const rail = ref(false)

  const items = [
    { title: 'Pedidos', icon: 'mdi-food', to: '/ped' },
    { title: 'Localização', icon: 'mdi-store-marker', to: '/' },
    { title: 'Funcionamento', icon: 'mdi-store-clock', to: '/' },
    { title: 'Promoções', icon: 'mdi-cart-percent', to: '/' },
    { title: 'Venha Buscar  ', icon: 'mdi-truck-delivery', to: '/' },
  ]
</script>
