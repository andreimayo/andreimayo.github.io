<script>
    import "../app.css";
    export const prerender = true;

</script>

<svelte:head>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous">
<link href="https://fonts.googleapis.com/css2?family=Afacad:ital,wght@0,400..700;1,400..700&display=swap" rel="stylesheet">
</svelte:head>

<main class="bg-gradient-to-r from-gray-900 to-gray-700 text-2xl font-bold">
    <div class="flex gap-4">
    <a href="/" class="underline text-indigo-600">Home</a>
    <a href="/portfolio" class="underline text-indigo-600">Portfolio</a>
    <a href="/about" class="underline text-indigo-600">About</a>
    <a href="/contact" class="underline text-indigo-600">Contact</a>
    
</div>
<slot></slot>
</main>

