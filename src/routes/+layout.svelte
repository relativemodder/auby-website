<script>
    import "../app.css";
</script>

<svelte:head>
    <title>Auby</title>
</svelte:head>


<h1 class="text-center mt-20 text-6xl font-bold">
    Auby
</h1>
<h2 class="mt-10 my-3 text-4xl px-8 flex flex-wrap w-full justify-center font-semibold">
    That one Geometry Dash 
    mod collection for iOS
</h2>

<div class="w-full flex justify-center">
    <div class="page-content">
        <slot />
    </div>
</div>