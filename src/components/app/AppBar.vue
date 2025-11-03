<template>
  <v-app-bar>

    <template v-if="$vuetify.display.mdAndUp" #append>
      <div class="hidden-sm-and-down">
        <v-btn
          v-for="item in menu"
          :key="item"
          class="text-body-1 blue-grey-darken-4"
          :href="`#${item.toLowerCase()}`"
          variant="text"
        >
          {{ item }}
        </v-btn>
      </div>
    </template>
  </v-app-bar>
</template>

<script setup>
  const menu = [
    'Home',
    'Funcionamento',
    'Localização',
    'Pedidos',
    'Promoções',
    'Venha Buscar',
  ]
</script>
