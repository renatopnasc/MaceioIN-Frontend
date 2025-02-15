<script setup>
import { Icon } from '@iconify/vue'
import {
  NavigationMenuContent,
  NavigationMenuItem,
  NavigationMenuList,
  NavigationMenuRoot,
  NavigationMenuTrigger,

} from 'radix-vue'
</script>


<template>
    <header class="w-full">
      <div class="w-full bg-[#f58428]">
        <ul class="max-w-6xl w-full mx-auto flex items-center py-3.5">
          <li>
            <a href="/" class=" text-sm uppercase font-bold text-white py-1 px-2.5 hover:text-[#14467C] transition-all duration-200">transparência</a>
          </li>
          <li class="ml-2.5 pl-2.5 border-l border-white">
            <a href="/" class=" text-sm uppercase font-bold text-white py-1 px-2.5 hover:text-[#14467C] transition-all duration-200">ouvidoria</a>
          </li>
          <li class="ml-2.5 pl-2.5 border-l border-white">
            <a href="/" class=" text-sm uppercase font-bold text-white py-1 px-2.5 hover:text-[#14467C] transition-all duration-200">diário oficial</a>
          </li>
          <li class="ml-2.5 pl-2.5 border-l border-white">
            <a href="/" class=" text-sm uppercase font-bold text-white py-1 px-2.5 hover:text-[#14467C] transition-all duration-200">covid-19</a>
          </li>
          <li class="ml-2.5 pl-2.5 border-l border-white">
            <a href="/" class=" text-sm uppercase font-bold text-white py-1 px-2.5 hover:text-[#14467C] transition-all duration-200">acesso à informação</a>
          </li>
        </ul>
      </div>
      <div class="max-w-6xl w-full mx-auto flex items-center justify-between">
        <figure>
          <img src="https://maceioalgovbr.dhost.cloud/assets/images/logo_prefeitura_de_maceio.svg" alt="">
        </figure>
        <figure>
          <img class="relative -bottom-1" src="https://maceioalgovbr.dhost.cloud/assets/images/maceio_topo.svg" alt="">
        </figure>
      </div>
      <div class="w-full bg-[#14467C] relative z-10">
        <NavigationMenuRoot class="max-w-6xl w-full flex items-center  mx-auto ">
          <NavigationMenuList class="flex gap-10">
            <NavigationMenuItem>
              <NavigationMenuTrigger class="text-base uppercase font-bold text-white cursor-pointer flex items-center gap-1 py-3.5">
                cidadão
                <Icon icon="radix-icons:caret-down"/>
              </NavigationMenuTrigger>
              <NavigationMenuContent class="absolute w-fit p-2 bg-[#f58428]">
                <ul>
                  <li><a href=""></a></li>
                </ul>
              </NavigationMenuContent>
            </NavigationMenuItem>
            

            <NavigationMenuItem>
              <NavigationMenuTrigger class="text-base uppercase font-bold text-white cursor-pointer flex items-center gap-1 py-3.5">
                servidor
                <Icon icon="radix-icons:caret-down"/>
              </NavigationMenuTrigger>
              <NavigationMenuContent class="absolute w-fit p-2 bg-[#f58428]">
                <ul>
                  <li><a href=""></a></li>
                </ul>
              </NavigationMenuContent>
            </NavigationMenuItem>

            <NavigationMenuItem>
              <NavigationMenuTrigger class="text-base uppercase font-bold text-white cursor-pointer flex items-center gap-1 py-3.5">
                empresário
                <Icon icon="radix-icons:caret-down"/>
              </NavigationMenuTrigger>
              <NavigationMenuContent class="absolute w-fit p-2 bg-[#f58428]">
                <ul>
                  <li><a href=""></a></li>
                </ul>
              </NavigationMenuContent>
            </NavigationMenuItem>

            <NavigationMenuItem>
              <NavigationMenuTrigger class="text-base uppercase font-bold text-white cursor-pointer flex items-center gap-1 py-3.5">
                turismo
                <Icon icon="radix-icons:caret-down"/>
              </NavigationMenuTrigger>
              <NavigationMenuContent class="absolute w-fit p-2 bg-[#f58428]">
                <ul>
                  <li><a href=""></a></li>
                </ul>
              </NavigationMenuContent>
            </NavigationMenuItem>

            <NavigationMenuItem>
              <NavigationMenuTrigger class="text-base uppercase font-bold text-white cursor-pointer flex items-center gap-1 py-3.5">
                imprensa
                <Icon icon="radix-icons:caret-down"/>
              </NavigationMenuTrigger>
              <NavigationMenuContent class="absolute w-fit p-2 bg-[#f58428]">
                <ul>
                  <li><a href=""></a></li>
                </ul>
              </NavigationMenuContent>
            </NavigationMenuItem>

            <NavigationMenuItem>
              <NavigationMenuTrigger class="text-base uppercase font-bold text-white cursor-pointer flex items-center gap-1 py-3.5">
                secretarias e órgãos
                <Icon icon="radix-icons:caret-down"/>
              </NavigationMenuTrigger>
              <NavigationMenuContent class="absolute w-fit p-2 bg-[#f58428]">
                <ul>
                  <li><a href=""></a></li>
                </ul>
              </NavigationMenuContent>
            </NavigationMenuItem>
          </NavigationMenuList>
        </NavigationMenuRoot>
      </div>
     </header>
</template>