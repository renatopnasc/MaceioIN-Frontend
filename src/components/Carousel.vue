<script setup lang="ts">
import { register } from 'swiper/element/bundle';
import CarouselItem from './CarouselItem.vue';
import {PhUsers,PhCalendar, PhFileText} from '@phosphor-icons/vue'

register()

type NewsItem = {
  icon: typeof PhCalendar | typeof PhFileText | typeof PhUsers; 
  title: string;
  date: string;
  description: string;
}

const news: NewsItem[] = [
  {
    icon: PhCalendar,
    title: "Calendário Fiscal 2025",
    date: "14/02/2025",
    description: "Confira as datas de vencimento dos tributos municipais para 2025. Planeje seus pagamentos e evite juros."
  },

  {
    icon: PhUsers,
    title: "Programa de Capacitação SEFAZ",
    date: "13/02/2025",
    description: "Novos cursos disponíveis para servidores da SEFAZ. Inscrições abertas para workshops e treinamentos."
  },

  {
    icon: PhFileText,
    title: "Atualização do Sistema Tributário",
    date: "12/02/2025",
    description: "Sistema tributário passará por manutenção programada. Confira os horários de indisponibilidade."
  }
]

</script>

<template>
    <swiper-container  class="h-full w-full" :navigation="true" :autoplay="{ delay: 10000, disableOnInteraction: false }">
      <CarouselItem v-for="sefazNew in news" :icon="sefazNew.icon" :title="sefazNew.title" :date="sefazNew.date" :description="sefazNew.description"/>
    </swiper-container>
</template>