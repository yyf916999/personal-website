<script>
  let experiences = [
    {
      role: "Software Engineer",
      company: "Nagrastar LLC",
      period: "JUL 2022 - Present",
      description: [
        "•	Designed and implemented a full-stack application for management of a company core application with 600+ instances using Python Flask and JavaScript. Reduced the resource needed for maintenance and monitor by 200%.",
        "•	Designed and implemented REST protocol to existing C++ applications, improving performance by 50% and increasing reliability. ",
        "•	Implemented a dashboard in Golang using Grafanna and Prometheus to help display healthcheck status of other applications in the system, reducing resource needed for monitoring by 100%.",
        "•	Regularly maintained testing environment in Kubernetes, updated application versions using docker, and improved CI/CD pipeline in Gitlab.",
      ],
      skills: [
        "devicon-javascript-plain colored",
        "devicon-django-plain colored",
        "devicon-docker-plain colored",
        "devicon-kubernetes-plain colored",
        "devicon-go-plain colored",
      ],
    },
    {
      role: "Co-Founder & CTO",
      company: "Blossoms AI",
      period: "MAR 2023 - APR 2024",
      description: [
        "•	As CO-Founder & CTO, I designed our software architecture and oversaw core strategies and product roadmap. Led a development team of 3 members for development work. After demoing our product to hundreds of teachers, we have received interests from 10 teachers in integrating our product into their curriculum.",
        "•	Designed and implemented a full-stack application in Reactjs and Python Flask, while utilizing fine-tuned GPT model to design personalized study plan in order to provide students the best education experience. Designed algorithms to optimize application performance, which resulted in a 200% improvement in performance result.",
        "•	Designed and implemented a production database in PostgreSQL and hosted the main application in AWS.",
      ],
      skills: [
        "devicon-postgresql-plain colored",
        "devicon-amazonwebservices-plain colored",
        "devicon-flask-original colored",
      ],
    },
    {
      role: "Apprentice",
      company: "Tianjin University",
      period: "MAY 2021 - AUG 2021",
      description: [
        "•	Helped design and implement a course evaluation application in C++ which let students evaluate their professors based on their experience taking the course.",
        "•	This helped other students choose their ideal classes in the future, which helped hundreds of students with their course registration dilemma.",
      ],
      skills: ["devicon-cplusplus-plain colored"],
    },
  ];
</script>

<section id="work-experience">
  <h2>Work Experience</h2>
  <div class="experience-list">
    {#each experiences as { role, company, period, description, skills }}
      <div class="experience-item">
        <div class="period">{period}</div>
        <div class="details">
          <h4>{role} at {company}</h4>
          {#each description as desc}
            <p class="work-desc">{desc}</p>
          {/each}
          {#each skills as skill}
            <i class={skill}></i>
          {/each}
        </div>
      </div>
    {/each}
  </div>
</section>

<style>
  #work-experience {
    padding: 2rem;
    background: white;
  }
  i {
    font-size: 1.5rem;
    margin-right: 1rem;
  }
  h2 {
    /* text-align: left; */
    font-size: 6rem;
    margin-left: 5%;
    /* margin-bottom: 2rem; */
  }
  .work-desc {
    font-size: 1.1rem;
    max-width: max-content;
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
