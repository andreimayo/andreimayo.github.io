<script>
   
    const socialLinks = [
      {
        platform: "Facebook",
        url: "https://www.facebook.com/andrei.mayo.3?mibextid=ZbWKwL", 
        icon: "fab fa-facebook" 
      },
      {
        platform: "Instagram",
        url: "https://www.instagram.com/andr.myo?igsh=ZGUzMzM3NWJiOQ==", 
        icon: "fab fa-instagram" 
      },
      {
        platform: "GitHub",
        url: "https://github.com/andreimayo", 
        icon: "fab fa-github" 
      },
    ];
  </script>
  
  <svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  </svelte:head>
  
  <main class="container mx-auto p-8 min-h-screen">
    <section class="text-center mb-12">
      <h1 class="text-5xl font-bold text-gray-700">Contact Me</h1>
      <p class="text-lg text-gray-600 mt-4">Feel free to reach out via social media!</p>
    </section>
  
    <section class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each socialLinks as link}
        <div class="bg-gray-900 p-6 rounded-lg shadow-lg text-center">
          <a href={link.url} target="_blank" rel="noopener noreferrer" class="flex flex-col items-center">
            <i class={link.icon + " text-4xl mb-4"}></i>
            <h2 class="text-2xl font-bold text-indigo-600 mb-2">{link.platform}</h2>
            <p class="text-gray-600">Follow me on {link.platform}</p>
          </a>
        </div>
      {/each}
    </section>
  </main>
  
  <style>
    main {
      font-family: 'Roboto', sans-serif;
    }
  </style>
  