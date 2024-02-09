<script>
  import { fly } from 'svelte/transition';
  import { onMount } from 'svelte';

  let skills = [
    { name: 'Python', level: 3 },
    { name: 'SQL', level: 3 },
    { name: 'Program Management', level: 4 },
    { name: 'Data Analysis', level: 5 },
    {name: 'Excel', level: 4},
  ];

  function animateBars() {
    skills.forEach((skill, index) => {
      setTimeout(() => {
        skills[index].level = skill.level; // Reset the level to trigger animation
      }, 100 * index);
    });
  }

  onMount(() => {
    animateBars();
  });
</script>

<div class="full-page-center">
  <h2 class="chart-header">My Skills</h2>
  <div class="chart-container">
    {#each skills as { name, level }}
      <div class="chart-row">
        <div class="skill-name">{name}</div>
        <div class="skill-bar-container">
          <div class="skill-bar" in:fly={{ x: -100, duration: 1000 }} style="width: {level * 20}%"></div>
        </div>
      </div>
    {/each}
  </div>

  <div class="learning-section">
    <h3 class="learning-header">What I'm Learning Right Now</h3>
    <p class="learning-description">
      Currently, I am working on expanding my web dev skills, AI development focusing on Mojo, and UI/UX knowledge. 
    </p>
    <img src="images/mojo.png" alt="mojo" class="learning-image" />
    <img src="images/js.png" alt="js" class="learning-image" />
    <img src="images/ux.png" alt="ux" class="learning-image"/>
  </div>
</div>


<style>
.full-page-center {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  min-height: 100vh;
  padding: 45px;
  background-image: linear-gradient(to bottom, var(--color-dark-blue), var(--color-accent-blue));
}

.chart-header {
  margin-bottom: 20px; /* Increase spacing between chart and learning section */
  color: #ffffff;
  text-align: center;
}

.chart-container {
  max-width: 600px;
  width: 80%;
  margin: 5px auto;
  padding: 40px; /* Increase padding for better separation */
  background: #082032;
  border-radius: 10px;
  box-shadow: 0 0px 15px #334756;
  text-align: center; /* Center text within the chart container */
}

.chart-row {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
}

.skill-name {
  flex: 1;
  font-weight: bold;
  color: #ffffff;
}

.skill-bar-container {
  flex: 3;
  background: #082032;
  border-radius: 5px;
  overflow: hidden;
}

.skill-bar {
  height: 30px;
  background-color: #FF4C29;
  border-radius: 5px 0 0 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.learning-section {
  width: 50%;
  padding: 12px;
  background: #082032;
  border-radius: 10px;
  box-shadow: 0 0px 15px #2C394B;
  color: #ffffff;
  text-align: center;
  margin: 20px auto;
}

.learning-header {
  font-size: 24px;
  margin-bottom: 5px;
}

.learning-description {
  font-size: 16px;
}

.learning-image { 
  justify-content: center;
  align-items: center;
  width: 40px;
  height: 40px;
  margin-right: 5px;
}


</style>



