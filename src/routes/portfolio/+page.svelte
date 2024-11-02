<script>

  
    
    const projects = [
      {
        title: "Shoe Stock",
        description: "A Shoe Stock is a software application designed to help retail stores or warehouses manage their shoe inventory efficiently.",
        technologies: ["JS", "HTML", "CSS"],
        images: [ 
          "/images/shoestock1.jpg", 
          "/images/shoestock2.jpg"  
        ],
        video: "https://drive.google.com/file/d/1fGOwkoG5H-GWUS4g9y8PjD5z_w40bq8n/view?usp=drivesdk" 
      },
      {
        title: "Calculator",
        description: "A Simple Calculator is a basic software application designed to perform common arithmetic operations such as addition, subtraction, multiplication, and division.",
        technologies: ["JS", "HTML", "CSS"],
        images: [ 
          "/images/calculator.jpg", 
          "/images/calculator.jpg"  
        ],
        video: "https://drive.google.com/file/d/1fMe8tB67RelkRWvHEvwhU8QUgBX6RvUC/view?usp=drivesdk" 
      },
      {
        title: "Home Inventory Manager",
        description: "A Home Inventory System is a software application designed to help users organize and track their household items.",
        technologies: ["JS", "HTML", "CSS"],
        images: [ 
          "/images/HomeInventory.jpg", 
          "/images/HomeInventory2.jpg"  
        ],
        video: "https://www.loom.com/share/51bf3a9cfdad487bac98ea32d1e77d92?sid=0cac1a45-d599-4d90-bed5-41060c91398c" // Add video link for this project
      },
    ];
  </script>
  
  <main class="container mx-auto p-8 min-h-screen">
    
    <section class="text-center mb-12">
      <h1 class="text-5xl font-bold text-gray-700">My Projects</h1>
      <p class="text-lg text-gray-600 mt-4">
        Here are some of the projects I’ve worked on.
      </p>
    </section>
  
    
    <section class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each projects as project}
        <div class="bg-black p-6 rounded-lg shadow-lg transition-transform transform hover:scale-105">
          {#if project.images}
            
            {#each project.images as image}
              <img src={image} alt={project.title} class="w-full h-48 object-cover rounded-lg mb-4">
            {/each}
          {/if}
          <h2 class="text-2xl font-bold text-indigo-600 mb-2">{project.title}</h2>
          <p class="text-gray-600 mb-4">{project.description}</p>
          <p class="text-sm text-gray-500 mb-4">
            <strong>Technologies:</strong> 
            {#each project.technologies as tech}
              {tech}{#if tech !== project.technologies[project.technologies.length - 1]}, {/if}
            {/each}
          </p>
          {#if project.video}
            <a href={project.video} target="_blank" rel="noopener noreferrer"  class="text-blue-500 font-semibold underline">
              Watch Demo
            </a>
          {/if}
        </div>
      {/each}
    </section>
  </main>
  
  <style>
    main {
      font-family: 'Roboto', sans-serif;
    }
  </style>
  