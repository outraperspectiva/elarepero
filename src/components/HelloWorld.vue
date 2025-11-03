<template>
  <v-container class="fill-height" max-width="900">
    <div>
      <v-img
        class="mb-8 mx-auto"
        height="600"
        src="@/assets/foodtruck.png"
      />

      <div class="mb-8 text-center">
        <div class="text-body-2 font-weight-light mb-n1">Bem Vindo à Lanchonete</div>
        <h1 class="text-h2 font-weight-bold">El Arepero</h1>
      </div>

      <v-row>
        <v-col cols="12">
          <v-card
            class="py-4"
            color="surface-variant"
            image="@/assets/ped.png"
            prepend-icon="mdi-food"
            rounded="lg"
            variant="tonal"
          >
            <template #image>
              <v-img position="top right" />
            </template>

            <template #title>
              <h2 class="text-h5 font-weight-bold">
                Venha se deliciar com nossos lanches!
              </h2>
            </template>

            <template #subtitle>
              <div class="text-subtitle-1">
                Faça um novo pedido com a gente.
              </div>
            </template>
          </v-card>
        </v-col>

        <v-col v-for="link in links" :key="link.href" cols="6">
          <v-card
            append-icon="mdi-open-in-new"
            class="py-4"
            color="surface-variant"
            :href="link.href"
            :prepend-icon="link.icon"
            rel="noopener noreferrer"
            rounded="lg"
            :subtitle="link.subtitle"
            target="_blank"
            :title="link.title"
            variant="tonal"
          />
        </v-col>
      </v-row>
    </div>
  </v-container>
</template>

<script setup lang="ts">
  const links = [
    {
      href: 'https://www.google.com/maps',
      icon: 'mdi-store-marker',
      subtitle: 'Saiba onde estamos trabalhando hoje',
      title: 'Localização',
    },
    {
      href: '',
      icon: 'mdi-store-clock',
      subtitle: 'Conheça nossos horários de atendimento.',
      title: 'Funcionamento',
    },
    {
      href: '',
      icon: 'mdi-cart-percent',
      subtitle: 'Descubra nossas promoções especiais.',
      title: 'Promoções',
    },
    {
      href: '',
      icon: 'mdi-truck-delivery',
      subtitle: 'Saiba mais sobre o tempo para sua entrega.',
      title: 'Venha Buscar',
    },
  ]
</script>
