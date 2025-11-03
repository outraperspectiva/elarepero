<template>
  <v-sheet
    id="sobre"
    class="py-16 text-center"
    color="secondary"
  >
    <div class="text-h4 font-weight-bold">
      O que fazemos
    </div>

    <div class="text-body-1 font-weight-regular mt-3 text-medium-emphasis mb-12">
      Descubra como nossa equipe incrível pode ajudar seu negócio.
    </div>

    <v-container>
      <v-row>
        <v-col
          v-for="item in whatWeDo"
          :key="item.title"
          class="d-flex flex-column align-center"
          cols="12"
          md="4"
        >
          <img :src="item.icon">

          <div class="text-h6 mt-1">
            {{ item.title }}
          </div>

          <div class="text-body-1 mt-2 text-medium-emphasis w-75">
            {{ item.description }}
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-sheet>
</template>

<script setup>
  const whatWeDo = [
    {
      icon: './assets/what/analytics.png',
      title: 'Google Analitycs',
      description:
        'Curabitur quam etsum lacus net netsum nulat iaculis etsimun vitae etsum nisle varius netsum',
    },
    {
      icon: './assets/what/awareness.png',
      title: 'Brand Awareness',
      description:
        'Curabitur quam etsum lacus net netsum nulat iaculis etsimun vitae etsum nisle varius netsum',
    },
    {
      icon: './assets/what/design.png',
      title: 'Graphic Design',
      description:
        'Curabitur quam etsum lacus net netsum nulat iaculis etsimun vitae etsum nisle varius netsum',
    },
  ]
</script>
