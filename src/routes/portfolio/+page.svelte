<script>
  // Sample data for your projects
  const projects = [
    {
      title: "Shoe Stock",
      description: "A machine learning project that classifies images using a neural network.",
      technologies: ["Python", "TensorFlow", "Keras"],
      images: [ // Array of images
        "src/images/shoestock1.png", // Ensure this path is correct
        "src/images/shoestock2.png"  // Ensure this path is correct
      ]
    },
    {
      title: "Personal Portfolio Website",
      description: "A personal portfolio website built with SvelteKit and Tailwind CSS.",
      technologies: ["SvelteKit", "Tailwind CSS", "JavaScript"],
      link: "https://github.com/username/portfolio-website",
      image: "/path-to-image.jpg",
    },
    {
      title: "Algorithm Visualizer",
      description: "A web-based application to visualize algorithms such as sorting and pathfinding.",
      technologies: ["JavaScript", "React", "D3.js"],
      image: "/path-to-shoestock1.png",
    },
  ];
</script>

<main class="container mx-auto p-8 min-h-screen">
  <!-- Page Title -->
  <section class="text-center mb-12">
    <h1 class="text-5xl font-bold text-gray-800">My Projects</h1>
    <p class="text-lg text-gray-600 mt-4">
      Here are some of the projects I’ve worked on.
    </p>
  </section>

  <!-- Project Cards -->
  <section class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
    {#each projects as project}
      <div class="bg-white p-6 rounded-lg shadow-lg transition-transform transform hover:scale-105">
        {#if project.images}
          <!-- Loop through the images array and display each image -->
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
        {#if project.image}
          <a href={project.image} target="_blank" rel="noopener noreferrer" class="text-blue-500 font-semibold hover:underline">
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
