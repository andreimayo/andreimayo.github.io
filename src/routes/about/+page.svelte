<script>
  
    const about = {
      name: "Andrei Mayo",
      title: "Third Year / BSCS",
      bio: " Hi there! I'm a third-year student majoring in computer science who is passionate about invention and technology. I like to experiment with several computer science fields, such as web technologies, machine learning, and software development.",
      image: "/images/profileimage.jpg", 
      interests: [
        { category: "Professional Interests", list: ["Web Development", "Game Development", "CyberSecurity"] },
        { category: "Frameworks", list: ["Svelte", "React", "Angular"] },
        { category: "Languages", list: ["Php", "JavaScript", "Python"] },
      ],
      skills: [
        "Communication",
        "Collaboration",
        "Testing",
        "Debugging",
      ],
    };
  </script>
  
  <main class="container mx-auto p-8 min-h-screen">
    
    <section class="text-center mb-12">
      <h1 class="text-5xl font-bold text-gray-700">About Me</h1>
      <p class="text-lg text-gray-500 mt-4">
        Learn more about my journey, skills, and professional interests.
      </p>
    </section>
  
   
    <section class="flex flex-col items-center md:flex-row md:items-start mb-12">
      
      {#if about.image}
        <!-- svelte-ignore a11y-img-redundant-alt -->
        <img
          src={about.image}
          alt="Profile Picture"
          class="w-48 h-48 rounded-full border-4 border-black shadow-lg mb-6 md:mb-0 md:mr-8 "
        />
      {/if}
  
      
      <div class="max-w-2xl">
        <h2 class="text-3xl font-bold text-gray-500 mb-4">{about.name}</h2>
        <p class="text-lg text-gray-500 mb-4">{about.title}</p>
        <p class="text-gray-500 mb-6">
          {about.bio}
        </p>
  
        
        <h3 class="text-2xl font-semibold text-gray-700 underline mb-4">Interests</h3>
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
          {#each about.interests as interests}
            <div class="bg-black p-4 rounded-lg shadow-md">
              <h4 class="text-xl font-semibold text-indigo-600 mb-2">{interests.category}</h4>
              <ul class="list-disc list-inside text-gray-700">
                {#each interests.list as item}
                  <li>{item}</li>
                {/each}     
              </ul>
            </div>
          {/each}
        </div>
      </div>
    </section>
  

    <section class="mb-12">
      <h3 class="text-2xl font-semibold text-indigo-600 mb-4">Soft and Hard Skills</h3>
      <ul class="list-disc list-inside text-gray-700">
        {#each about.skills as skills}
          <li>{skills}</li>
        {/each}
      </ul>
    </section>
  </main>
  
  <style>
    main {
      font-family: 'Roboto', sans-serif;
    }
  </style>
  