<script>
  let experiences = [
    {
      role: "Editor",
      company: "ABC Corp",
      period: "2035 - Present",
      description:
        "I'm a paragraph. Click here to add your own text and edit me. It’s easy. Just click 'Edit Text' or double click me to add your own content and make changes to the font.",
    },
    {
      role: "Writer at Large",
      company: "XYZ Ltd",
      period: "2035 - 2035",
      description:
        "I'm a paragraph. Click here to add your own text and edit me. It’s easy. Just click 'Edit Text' or double click me to add your own content and make changes to the font.",
    },
    {
      role: "Intern",
      company: "123 Inc",
      period: "2035 - 2035",
      description:
        "I'm a paragraph. Click here to add your own text and edit me. It’s easy. Just click 'Edit Text' or double click me to add your own content and make changes to the font.",
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
