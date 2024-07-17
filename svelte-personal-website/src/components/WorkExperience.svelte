<script>
  let experiences = [
    {
      role: "Software Engineer",
      company: "Nagrastar LLC",
      period: "JUL 2022 - Present",
      description:
        "Designed and developed multiple full-stack web application. Regularly maintained testing environment and CI/CD pipeline.",
    },
    {
      role: "Co-Founder & CTO",
      company: "Blossoms AI",
      period: "MAR 2023 - APR 2024",
      description:
        "Designed and developed a full-stack web application that integrates AI to help improve students' learning experience by identifying subjects and areas at which the student is lacking.",
    },
    {
      role: "Apprentice",
      company: "Tianjin University",
      period: "MAY 2021 - AUG 2021",
      description:
        "Made a course-evaluation application to help students to have a better idea when course selection time comes.",
    },
  ];
</script>

<section id="work-experience">
  <h2>Work Experience</h2>
  <div class="experience-list">
    {#each experiences as { role, company, period, description }}
      <div class="experience-item">
        <div class="period">{period}</div>
        <div class="details">
          <h4>{role} at {company}</h4>
          <p>{description}</p>
        </div>
      </div>
    {/each}
  </div>
</section>

<style>
  #work-experience {
    padding: 2rem;
    background-color: #f9f9f9;
  }

  h2 {
    /* text-align: left; */
    font-size: 7rem;
    /* margin-left: 10%; */
    /* margin-bottom: 2rem; */
  }

  .experience-list {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  .experience-item {
    display: flex;
    align-items: flex-start;
  }

  .period {
    font-size: 1rem;
    color: #333;
    width: 25%;
    min-width: 150px; /* Ensures the date section has a minimum width */
    text-align: right;
    padding-right: 1rem;
  }

  .details {
    font-size: 1rem;
    width: 75%;
  }

  .details h4 {
    margin: 0;
    font-size: 1.2rem;
    font-weight: bold;
  }

  .details p {
    margin: 0.5rem 0 0 0;
    color: #555;
  }
</style>
