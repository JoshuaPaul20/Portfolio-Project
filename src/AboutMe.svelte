<!-- src/AboutMe.svelte -->

<section class="about-me">
  <h2>Hi ✋</h2>
  <h3>I'm Joshua <span class="highlight">Paul</span></h3>
  <img src="images/Josh.PNG" alt="Joshua Paul" />
  <p>I am an Innovator, Programmer, & Business Analyst</p>

  <div class="table-container">
    <table class="about-details">
      <tr>
        <th>ID</th>
        <th>Education</th>
        <th>Occupation</th>
        <th>Experience</th>
      </tr>
      <tr>
        <td>Joshua</td>
        <td>Business Analytics, Bellevue University</td>
        <td>USAF Training Manager</td>
        <td>9 Years USAF</td>
      </tr>
    </table>
  </div>

</section>

<style>
  .about-me {
    text-align: center;
    padding: 80px;
    background-image: linear-gradient(to bottom, var(--color-dark-blue), var(--color-accent-blue));
    border-radius: 8px;
    font-family: 'Roboto', sans-serif;
  }

  .about-me img {
    width: 250px; 
    height: auto;
    border-radius: 30%;
    margin-top: 20px;
    box-shadow: 0 0px 15px #FF4C29;
    transition: box-shadow 0.3s ease-out;
  }

  .about-me img:hover {
    box-shadow: 0 0px 40px #FF4C29;
  }

  .about-me p {
    margin: 20px auto;
    line-height: 1.8;
    max-width: 80%;
  }

  .highlight {
    color: #FF4C29;
    font-size: 150%;
  }

  .table-container {
    text-align: center;
    margin: 20px auto;
    width: 80%;
  }

  .about-details {
    border-collapse: collapse;
    width: 100%;
  }

  .about-details th, .about-details td {
    padding: 8px 16px;
  }

  .about-details th {
    background-color: #082032;
    color: #ffffff;
  }

  .about-details tr:nth-child(even) {
    background-color: #2C394B;
  }


  @media (max-width: 600px) {
    .about-me {
      padding: 20px;
    }

  }
</style>
