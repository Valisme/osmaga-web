<script lang="ts">
import { writable } from "svelte/store";
import Bars from "./Bars.svelte";
import Sidebar from "./Sidebar.svelte";
import X from "./X.svelte";
let isOpen = false

$: console.log(isOpen)

</script>

<nav class="w-full h-20 lg:w-full lg:h-16 bg-blue-500 flex flex-row justify-end items-center pr-6 lg:pr-0">
    <ul class="hidden h-full lg:flex lg:flex-row gap-4 justify-start text-xl font-bold px-4 ">
       <li class="p-4 hover:bg-gray-300/50 rounded-xl">Beranda</li>
       <li >
        <div class="group flex flex-col justify-center text-center ">
            <div class="p-4 hover:bg-gray-300/50 rounded-xl rounded-b-none">Tentang Kami</div>
            <div class="p-4 invisible group-hover:visible bg-blue-500 z-[999]">Visi & Misi</div>
            <div class="p-4 rounded-b-xl invisible group-hover:visible bg-blue-500 z-[999]">Struktur Anggota</div>
        </div>
       </li> 
       <li class="p-4 hover:bg-gray-300/50 rounded-xl">Galeri</li> 
       <li class="p-4 hover:bg-gray-300/50 rounded-xl">Berita</li> 
       
    </ul>
    <button class="block lg:hidden" on:click={()=>isOpen = !isOpen} aria-hidden="true" tab-index="-1"><Bars/></button>
    {#if isOpen}
    <Sidebar bind:isOpen={isOpen}/>
    {/if}

</nav>