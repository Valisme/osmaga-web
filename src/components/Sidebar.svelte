<script lang="ts">
    export let isOpen:boolean;

</script>
{#if isOpen}
<div class="absolute h-full w-full bg-black/50 left-0 top-0" aria-hidden="true" on:click|self={()=>isOpen = !isOpen} >
    <!-- <button class="absolute right-4 top-4" on:click={()=>isisOpen = !isisOpen}><X/></button> -->
    <div class="h-full p-4 w-5/6 bg-black  relative">
        <ul class="text-white text-4xl flex flex-col gap-4">
            <li>Beranda</li>
            <li class="ho">
                <p>Tentang Kami</p>
            </li>
            <li>Galeri</li>
            <li>Blog</li>
        </ul>
        <button class="p-2 absolute bottom-8 right-8 bg-green-500 text-xl rounded-lg font-bold" on:click={()=>isOpen = !isOpen}> Tutup Kembali </button>
    </div>
</div>
{/if}
