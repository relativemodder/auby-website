<script lang="ts">
    export let href = "#";
    export let newTab = false;
    export let secondary = false;


    function goToLink(url: string, openInNewTab: boolean) {
        if (url == "#") return;
        if (openInNewTab) return window.open(url, '_blank')?.focus();
        location.assign(url);
    }

</script>

<a href={href}
    on:click|preventDefault={() => goToLink(href, newTab)}
    class={
        `${
            secondary 
            ? 'border-slate-900 border-solid border-2 text-white' 
            : 'bg-white text-black'
        } 
        flex items-center justify-center gap-5 p-6 px-20 text-2xl rounded-xl w-full max-w-96 
        ${
            secondary 
            ? 'active:border-slate-700' 
            : 'active:bg-red-700'
        } 
        transition`
    }
>
    <slot />
</a>