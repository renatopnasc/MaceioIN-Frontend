<script setup lang="ts">
    import { onMounted, ref } from 'vue';
    import axios from 'axios'

    interface Funcionarios {
        nome: string
        sobrenome: string
        email: string
        setor: string
    }

    let funcionarios = ref([] as Funcionarios[])

    onMounted(async () => {
    const response = await axios.get("http://localhost:8000/api/v1/funcionarios/", {
        withCredentials: true
    })

    funcionarios.value = response.data.funcionarios
    })
</script>

<template>
    <div class="overflow-y-auto max-h-96 w-full ">
            <table class="w-full">
              <thead>
                <tr class="border-b-[1px] border-neutral-200">
                  <th class="text-left w-[60%] bg-neutral-100 p-4 rounded-tl-2xl">Nome</th> 
                  <th class="text-left bg-neutral-100 p-4">Email</th>
                  <th class="text-left bg-neutral-100 p-4 rounded-tr-2xl">Setor</th>
                </tr>
              </thead>

              <tbody>
                <tr class="border-b-[1px] border-neutral-100" v-for="funcionario in funcionarios">
                  <td class="p-4 bg-white text-normal text-[#4F4F4F]">{{ funcionario.nome + " " + funcionario.sobrenome }}</td>
                  <td class="p-4 bg-white">
                    <a :href="'mailto:' + funcionario.email" class="text-[#14467c] font-semibold text-sm">{{ funcionario.email }}</a>
                  </td>
                  <td class="p-4 bg-white text-xs text-[#f58428] font-semibold"><span class="bg-orange-200 py-1 px-2 rounded-full">{{ funcionario.setor }}</span></td>
                </tr>
              </tbody>
            </table>
          </div>
</template>