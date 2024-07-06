<script>
  let skills = [
    {
      name: "HTML",
      icon: "devicon-html5-plain colored",
      details: "HTML is the standard markup language for creating web pages.",
    },
    {
      name: "CSS",
      icon: "devicon-css3-plain colored",
      details: "CSS is a language used to style HTML documents.",
    },
    {
      name: "JavaScript",
      icon: "devicon-javascript-plain colored",
      details:
        "JavaScript is a programming language used to create interactive effects within web browsers.",
    },
    {
      name: "React",
      icon: "devicon-react-plain colored",
      details: "React is a JavaScript library for building user interfaces.",
    },
    {
      name: "Python",
      icon: "devicon-python-plain colored",
      details:
        "Python is a programming language that lets you work quickly and integrate systems more effectively.",
    },
    {
      name: "Flask",
      icon: "devicon-flask-original colored",
      details:
        "Flask is a lightweight WSGI web application framework in Python.",
    },
    {
      name: "C/C++",
      icon: "devicon-cplusplus-plain colored",
      details:
        "C and C++ are general-purpose programming languages that are widely used for system and application software.",
    },
    {
      name: "GIT",
      icon: "devicon-git-plain colored",
      details:
        "Git is a distributed version-control system for tracking changes in source code during software development.",
    },
    {
      name: "Docker",
      icon: "devicon-docker-plain colored",
      details:
        "Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers.",
    },
    {
      name: "Kubernetes",
      icon: "devicon-kubernetes-plain colored",
      details:
        "Kubernetes is an open-source container-orchestration system for automating application deployment, scaling, and management.",
    },
    {
      name: "Go",
      icon: "devicon-go-plain colored",
      details:
        "Go is a statically typed, compiled programming language designed at Google.",
    },
    {
      name: "Linux",
      icon: "devicon-linux-plain colored",
      details: "Linux is a family of open-source Unix-like operating systems.",
    },
    {
      name: "Java",
      icon: "devicon-java-plain colored",
      details:
        "Java is a high-level, class-based, object-oriented programming language.",
    },
    {
      name: "Bash",
      icon: "devicon-bash-plain colored",
      details: "Bash is a Unix shell and command language.",
    },
    {
      name: "MySQL",
      icon: "devicon-mysql-plain colored",
      details: "MySQL is an open-source relational database management system.",
    },
    {
      name: "Jenkins",
      icon: "devicon-jenkins-plain colored",
      details: "Jenkins is an open-source automation server.",
    },
    {
      name: "PostgreSQL",
      icon: "devicon-postgresql-plain colored",
      details:
        "PostgreSQL is a powerful, open-source object-relational database system.",
    },
    {
      name: "Jira",
      icon: "devicon-jira-plain colored",
      details:
        "Jira is a proprietary issue tracking product developed by Atlassian.",
    },
  ];

  let selectedSkill = null;

  function showDetails(skill) {
    selectedSkill = skill;
  }
</script>

<section id="skills">
  <h2>Skills</h2>
  <div class="skill-content">
    <div class="skills-description">
      <p>Some tech-related skills I have learnt and used over the years.</p>
      <p>Click on each icon for more details</p>
    </div>
    <div class="skills-icons">
      <div class="skills-grid">
        {#each skills as skill}
          <div class="skill" on:click={() => showDetails(skill)}>
            <i class={skill.icon}></i>{skill.name}
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>

{#if selectedSkill}
  <div class="details-panel">
    <h2>{selectedSkill.name}</h2>
    <p>{selectedSkill.details}</p>
  </div>
{/if}

<style>
  .skill-content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: flex-start;
    text-align: left;
    margin: 0 auto;
    padding: 0 1rem;
    box-sizing: border-box;
  }

  .skills-description h3,
  .skills h3 {
    font-size: 1.5rem;
    margin-bottom: 1rem;
    font-weight: bold;
  }

  .skills-description p {
    margin-bottom: 1rem;
  }

  .skill-description {
    flex: 1;
  }

  .skill-icons {
    flex: 1;
  }

  .skills-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .skill {
    background-color: white;
    padding: 0.5rem 1rem;
    border-radius: 5px;
    font-size: 0.9rem;
    display: flex;
    align-items: center;
    cursor: pointer;
  }

  .skill i {
    margin-right: 0.5rem;
    font-size: 1.2rem;
  }

  section {
    padding: 2rem 1rem;
    background-color: #f0f0f0;
  }

  h2 {
    margin-bottom: 1rem;
    font-size: 2rem;
    font-weight: bold;
  }

  p {
    font-size: 1.1rem;
    line-height: 1.8;
  }

  .about-content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: flex-start;
    text-align: left;
    margin: 0 auto;
    padding: 0 1rem;
    box-sizing: border-box;
  }

  .description {
    flex: 1;
    margin-right: 5rem;
  }

  .software-pic {
    flex: 1;
  }

  .details-panel {
    margin-top: 2rem;
    padding: 1rem;
    background-color: #fff;
    border: 1px solid #ddd;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
</style>
