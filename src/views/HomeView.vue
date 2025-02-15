<script setup lang="ts">
import TheHeader from '@/components/TheHeader.vue';
import Carousel from '@/components/Carousel.vue';
import TheTable from '@/components/TheTable.vue';
</script>

<template>
  <div class="w-full min-h-screen bg-neutral-50 antialiased">
    <!-- Header -->
    <TheHeader/>

    <!-- Main -->
     <main class="w-full pt-12 flex flex-col gap-4 bg-neutral-50">
      <div class="max-w-6xl w-full mx-auto px-1">
        <!-- Main Header -->
        <section class="mb-30">
          <div class="mb-11">
            <h2 class="font-bold text-lg text-[#14467C] uppercase">sefaz</h2>
            <h1 class="font-bold text-[#14467c] text-3xl pb-3 border-b-4 border-[#f58428]">Secretaria Municipal de Fazenda</h1>
          </div>

          <p class=" font-normal leading-8 text-justify text-lg text-[#4F4F4F]">
            A <strong>Secretaria Municipal de Fazenda de Maceió (SEFAZ Maceió)</strong> é responsável pela gestão financeira e tributária do município, garantindo o equilíbrio fiscal e o desenvolvimento sustentável da cidade. Nossa missão é administrar os recursos públicos com transparência, eficiência e responsabilidade, promovendo a arrecadação justa e o controle adequado das finanças municipais.
          </p>
        </section>

        <!-- Novidades -->
        <section class="flex flex-col items-center mb-30">
          <h2 class="font-bold text-[#14467c] text-3xl mb-10">Novidades SEFAZ</h2>

          <div class="max-w-2xl w-full h-[400px] bg-white shadow rounded p-8">
            <Carousel/>
          </div>
        </section>

        <!-- Tabela funcionários -->
        <section class="mb-30 flex flex-col items-center">
          <h2 class="font-bold text-[#14467c] text-3xl mb-10">Colaboradores SEFAZ Maceió</h2>
          <TheTable/>
        </section>
      </div>
     </main>
  </div>
</template>
