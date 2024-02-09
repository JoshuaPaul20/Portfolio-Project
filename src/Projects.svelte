<!-- src/Projects.svelte -->

<section class="projects">
  <h2>Projects</h2>

  <!-- Center all content using flexbox -->
  <div class="center-container">
    <!-- Replace with your project cards or descriptions -->
    <div class="project-card">
      <div class="card-front">
        <img src="images/Narrative Tracker.jpg" alt="App Information" class="project-img" />
        <h3>Narrative Tracker</h3>
      </div>
      <div class="card-back">
        <p>Developed a dedicated mobile application tailored for members of the United States Air Force, providing a secure and centralized platform for tracking their EPB/OPB information. This initiative streamlined data management processes, ensuring convenience and confidentiality for personnel accessing critical information.</p>
        <div class="icons">
          <img src="images/swift.png" alt="Swift Icon" class="icon" />
          <img src="images/firebase.png" alt="Firebase Icon" class="icon" />
        </div>
      </div>
    </div>

    <div class="project-card">
      <div class="card-front">
        <img src="images/Strike.jpg" alt="Project Standoff Cargo" class="project-img" />
        <h3>Project Mercury Cohort 11</h3>
      </div>
      <div class="card-back">
        <p>Through the Project Mercury ecosystem, contributed to a team focused on extending cargo delivery capabilities in challenging environments. Our efforts culminated in the development of groundbreaking technology known as 'Standoff Cargo.' Additionally, attained certification as a Professional Innovator, underscoring dedication to pioneering advancements within the field.</p>
        <div class="icons">
          <img src="images/PM.png" alt="Project Mercury" class="icon" />
        </div>
      </div>
    </div>

    <div class="project-card">
      <div class="card-front">
        <img src="images/lms.jpg" alt="Training Program" class="project-img" />
        <h3>USAF Training Management</h3>
      </div>
      <div class="card-back">
        <p>Directed and oversaw the training program across various Air Force Learning Management Systems (AF LMS), demonstrating adept leadership. Effectively managed group training schedules, meticulously forecasting seat requests, handling out-of-cycle requests, and ensuring proper allocation of funding resources. Diligently compiled and analyzed training statistics, subsequently presenting comprehensive trend analysis briefs to inform strategic decision-making processes.</p>
        <div class="icons">
          <img src="images/training.png" alt="Training" class="icon" />
        </div>
      </div>
    </div>
    <!-- Add more project cards as needed -->
  </div>
</section>

<style>
  /* Add your CSS styles here to style the Projects section */
  .projects {
    /* Center horizontally and vertically */
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center; /* Center text within project cards */
    padding: 110px;
    background-image: linear-gradient(to bottom, var(--color-dark-blue), var(--color-accent-blue));
  }

  .center-container {
    display: flex;
    flex-wrap: nowrap;
    align-items: center;
  }

  .project-card {
    /* Add styling for project cards */
    margin: 60px; /* Add spacing between project cards */
    perspective: 1000px;
    width: 300px;
    height: 300px;
    border-radius: 20px;
  }

  .card-front,
  .card-back {
    width: 100%;
    height: 100%;
    position: absolute;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    backface-visibility: hidden;
    transition: transform 0.5s;
    border-radius: 15px;
  }

  .card-back {
    transform: rotateY(180deg);
    background: #fff;
    color: #333;
    padding: 20px;
  }

  .project-card:hover .card-front {
    transform: rotateY(180deg);
  }

  .project-card:hover .card-back {
    transform: rotateY(0deg);
  }

  .project-img {
    max-width: 400px;
    max-height: 400px;
  }

  .icons .icon {
    width: 35px; /* Adjust the icon size as needed */
    height: 35px; /* Adjust the icon size as needed */
    margin-right: 10px; /* Add spacing between icons */
    margin-bottom: 20px;
  }

  h2 {
    font-size: 200%;
  }
</style>