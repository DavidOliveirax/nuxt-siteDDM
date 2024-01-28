<template>
  <div>
    <Header />
  </div>
  <div class="h-96 flex justify-center items-center">
    <section>
      <h1
        class="bg-gradient-to-r from-gray-400 via-red-400 to-red-600 bg-clip-text text-3xl font-extrabold text-transparent sm:text-5xl">
        O SEU DESKTOP ESTÁ AQUI!
      </h1>
    </section>
  </div>
  <div>
    <UContainer>
      <UCard class="mt-10">
        <template #header>
          <div class="flex justify-between items-center">
            <h1 class="font-bold">DESKTOP HOME</h1>
            <USelect color="red" v-model="homeSelected" :options="homeOptions" />
          </div>
        </template>
        <div id="configD">
          <ModelosConfig3 v-if="homeSelected == 'i3'" />
          <ModelosConfig5 v-if="homeSelected == 'i5'" />
          <ModelosConfig7 v-if="homeSelected == 'i7'" />
        </div>
      </UCard>
      <UCard class="mt-10">
        <template #header>
          <div class="flex justify-between items-center">
            <h1 class="font-bold">DESKTOP GAMER MID</h1>
          </div>
        </template>
        <div class="flex justify-evenly items-center">
          <div>
            <img class="w-72 mb-20" src="@/assets/image/gamer-mid.png" alt="">
          </div>
          <div class="w-60 h-48">
            <h1 class="pb-5">
              AMD Ryzen 5 5600G <br>
              Placa Mãe B450 <br>
              RAM DDR4 16GB 3200mhz <br>
              SSD NVMe 500GB <br>
            </h1>
            <h1 class="text-red-600 font-bold text-3xl pb-8">R$3.190,00</h1>
            <UButton color="gray" icon="i-heroicons-arrow-right-circle-solid" to="https://ui.nuxt.com" target="_blank">
              Comprar
            </UButton>
          </div>
        </div>
      </UCard>
      <UCard class="mt-10">
        <template #header>
          <div class="flex justify-between items-center">
            <h1 class="font-bold">DESKTOP GAMER MAX</h1>
          </div>
        </template>
        <div class="flex justify-evenly items-center">
          <div>
            <img class="w-72 mb-20 " src="@/assets/image/gamer-max.png" alt="">
          </div>
          <div class="w-60 h-48">
            <h1 class="pb-5">
              AMD Ryzen 7 5700X <br>
              Placa Mãe B450 <br>
              RAM DDR4 16GB 3200mhz <br>
              SSD NVMe 1TB <br>
              Nvidia RTX 3060 <br>
            </h1>
            <h1 class="text-red-600 font-bold text-3xl pb-8">R$5.690,00</h1>
            <UButton color="gray" icon="i-heroicons-arrow-right-circle-solid" to="https://ui.nuxt.com" target="_blank">
              Comprar
            </UButton>
          </div>
        </div>
      </UCard>
    </UContainer>
  </div>
  <div>
    <Footer />
  </div>
</template>

<script setup>
const homeSelected = ref('i3')
const homeOptions = ref([
  {
    label: 'Desktop i3',
    value: 'i3'
  }, {
    label: 'Desktop i5',
    value: 'i5',
  }, {
    label: 'Desktop i7',
    value: 'i7'
  }
])
</script>

<style></style>