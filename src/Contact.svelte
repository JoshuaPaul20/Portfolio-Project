<!-- Contact.svelte -->
<script>
  // You can add any Svelte logic or data bindings here if needed
</script>

<style>
  /* Set up a flex container to align content at the bottom */
  .container {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    min-height: 100vh; /* Ensure the container takes up the full viewport height */
    text-align: center;
    background-image: linear-gradient(to bottom, var(--color-dark-blue), var(--color-accent-blue));
  }

  .contact {
    padding: 20px;
  }

  .contact p {
    margin: 10px 0;
  }

  .linkedin-logo {
    width: 40px; /* Adjust the size as needed */
    height: auto;
    vertical-align: middle;
    margin: 5px;
  }

  /* Style the divider */
  hr {
    border: 2px solid #ccc; /* You can adjust the color and style as needed */
    margin-top: 50px;
    margin-bottom: 400px;
  }

  .icon {
    width: 40px;
    height: 40px;
    margin-right: 5px;
  }

  /* Add a spacer to push content to the bottom */
  .spacer {
    flex-grow: 1;
  }
</style>

<div class="container">
  <section class="contact">
    <h2> Let's Connect </h2>
    <p>
      <a href="https://www.linkedin.com/in/joshua-paul-97451292/"><img src="images/linkedin.png" alt="LinkedIn" class="linkedin-logo"/></a>
      <a href="https://github.com/JoshuaPaul20"><img src="images/github.png" alt="Github" class="linkedin-logo"/></a>
    </p>
    <hr> <!-- Divider -->
    <h2> Built with: </h2>
    <p>
      <img src="images/svelte.png" alt="Icon 1" class="icon"/>
      <img src="images/netlify.png" alt="Icon 3" class="icon"/>
      <!-- Add more icons as needed -->
    </p>
  </section>
  <div class="spacer"></div> <!-- Spacer to push content to the bottom -->
</div>
