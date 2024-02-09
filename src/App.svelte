<script>
	import Router from 'svelte-spa-router';
	import AboutMe from './AboutMe.svelte';
	import Projects from './Projects.svelte';
	import Skills from './Skills.svelte';
	import Contact from './Contact.svelte';
  
	// Define your routes
	const routes = {
	  '/': AboutMe, // Home page
	  '/about': AboutMe, // About Me page
	  '/projects': Projects, // Projects page
	  '/skills': Skills, // Skills page
	  '/contact': Contact, // Contact page
	};
  </script>
  
  <nav>
	<img src="images/jp.png" alt="Logo" style="width: 60px; height: 60px; margin-right: 10px;">
	<ul>
	  <li><a href="#/">Home</a></li>
	  <li><a href="#/projects">Projects</a></li>
	  <li><a href="#/skills">Skills</a></li>
	  <li><a href="#/contact">Connect</a></li>
	</ul>
  </nav>
  
  <Router {routes} />
  
  <style>
	:global(body) {
	  font-family: 'Roboto', sans-serif;
	  --color-dark-blue: #082032;
	  --color-light-blue: #2C394B;
	  --color-accent-blue: #334756;
	  --color-highlight: #FF4C29;
	  background-color: #082032;
	  color: white; /* For contrast */
	  margin: 0;
	  padding: 0;
	  box-sizing: border-box;
	}
  
	nav {
	  padding: 1rem;
	  display: flex;
	  align-items: center;
	  justify-content: space-between;
	}
  
	nav ul {
	  list-style-type: none;
	  padding: 0;
	  display: flex;
	  justify-content: center;
	  align-items: center;
	  margin: 0;
	}
  
	nav li {
	  margin: 0 2rem;
	}
  
	nav a {
	  color: #ffff;
	  text-decoration: none;
	  transition: color 0.3s ease;
	}
  
	nav a:hover {
	  color: #FF4C29;
	}
  
	:global(button) {
	  background-color: var(--color-highlight);
	  color: white;
	  border: none;
	  padding: 10px;
	  border-radius: 5px;
	  transition: background-color 0.2s;
	}
  
	:global(button:hover) {
	  background-color: #FF4C29; /* A slightly darker shade of your highlight color for hover effect */
	}
	
	/* Layout Adjustments */
	:global(header), :global(footer), :global(main) {
	  padding: 1rem;
	  text-align: center;
	}
  
	:global(main) {
	  min-height: 80vh; /* Ensures that the main content takes up the majority of the viewport height */
	}
  
	:global(footer) {
	background-color: transparent;
	  color: white;
	  padding: 1rem 0;
	}
  </style>