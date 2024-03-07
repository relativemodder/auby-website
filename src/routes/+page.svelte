<script lang="ts">
    import Icon from '@iconify/svelte';
    import Button from "$lib/components/button.svelte";
    import { data } from "$lib";

    const aubyData = data;
</script>

<a href="/img/screenshot-main.png" target="_blank" class="transition">
    <img 
        class="shadow-red-950 shadow-2xl rounded-xl"
        src="/img/screenshot-main.png" 
        alt="GD Screenshot that says Auby v2 Experimental Build" />
</a>

<small class="text-center block text-gray-300 mt-2">Main screen</small>

<h2 class="text-center text-5xl mt-10 font-semibold">Features:</h2>

<div class="flex w-full justify-center mt-10 text-xl">
    <ul class="w-96">
        { #each aubyData.features as feature }
            <li class="flex items-center gap-2"><Icon icon="material-symbols:circle" style="scale: 0.6;" />{ feature }</li>
        { /each }
    </ul>
</div>

<div class="flex w-full justify-center my-10 mt-10 flex-col gap-8 items-center">
    <Button href={data.download} newTab>
        <Icon icon="material-symbols:download" style="transform: scale(1.3);" />
        <span>Download</span>
    </Button>
    <Button secondary href={data.discord} newTab>
        <Icon icon="ic:baseline-discord" style="transform: scale(1.3);" />
        <span>Discord</span>
    </Button>
    <Button secondary href={data.github} newTab>
        <Icon icon="mdi:github" style="transform: scale(1.3);" />
        <span>GitHub</span>
    </Button>
</div>