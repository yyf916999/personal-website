<script>
  let experiences = [
    {
      period: "2035 - Present",
      position: "Web Content Writer",
      company: "My Bite",
      location: "San Francisco, Cal.",
    },
    {
      period: "2035 - 2035",
      position: "Content Writer",
      company: "Unilife",
      location: "Manhattan, New York",
    },
    {
      period: "2035 - 2035",
      position: "Content Writer Intern",
      company: "InspirationIT",
      location: "San Francisco, Cal.",
    },
  ];
</script>

<section id="work-experience">
  <div class="header">
    <h2>WORK EXPERIENCE</h2>
    <a class="resume-button" href="/assets/resume.pdf" download
      >Download Resume</a
    >
  </div>
  <div class="experience-list">
    {#each experiences as experience}
      <div class="experience-item">
        <p class="period"><strong>{experience.period}</strong></p>
        <p class="position">{experience.position}</p>
        <p class="company">{experience.company}</p>
        <p class="location"><em>{experience.location}</em></p>
      </div>
    {/each}
  </div>
</section>

<style>
  #work-experience {
    padding: 2rem;
    background-color: #fff;
  }

  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 2rem;
  }

  h2 {
    font-size: 2rem;
    position: relative;
  }

  h2::after {
    content: "";
    display: block;
    width: 50px;
    height: 2px;
    background: black;
    margin: 0.5rem auto 0;
  }

  .resume-button {
    background-color: #f04e4e;
    color: white;
    padding: 0.75rem 1.5rem;
    border: none;
    border-radius: 5px;
    text-decoration: none;
    font-size: 1rem;
    cursor: pointer;
  }

  .resume-button:hover {
    background-color: #d43d3d;
  }

  .experience-list {
    max-width: 800px;
    margin: 0 auto;
  }

  .experience-item {
    margin-bottom: 2rem;
  }

  .period {
    font-size: 1.1rem;
  }

  .position {
    font-size: 1.2rem;
    font-weight: bold;
  }

  .company,
  .location {
    font-size: 1rem;
    color: gray;
  }
</style>
