<script>
  let skills = [
    { name: "HTML", icon: "devicon-html5-plain colored" },
    { name: "CSS", icon: "devicon-css3-plain colored" },
    { name: "JavaScript", icon: "devicon-javascript-plain colored" },
    { name: "React", icon: "devicon-react-plain colored" },
    { name: "Python", icon: "devicon-python-plain colored" },
    { name: "Flask", icon: "devicon-flask-original colored" },
    { name: "C/C++", icon: "devicon-cplusplus-plain colored" },
    { name: "GIT", icon: "devicon-git-plain colored" },
    { name: "Docker", icon: "devicon-docker-plain colored" },
    { name: "Kubernetes", icon: "devicon-kubernetes-plain colored" },
    { name: "Go", icon: "devicon-go-plain colored" },
    { name: "Linux", icon: "devicon-linux-plain colored" },
    { name: "Java", icon: "devicon-java-plain colored" },
    { name: "Bash", icon: "devicon-bash-plain colored" },
    { name: "Java", icon: "devicon-java-plain colored" },
    { name: "MySQL", icon: "devicon-mysql-plain colored" },
    { name: "Jenkins", icon: "devicon-jenkins-plain colored" },
    { name: "PostgreSQL", icon: "devicon-postgresql-plain colored" },
    { name: "Jira", icon: "devicon-jira-plain colored" },
  ];
</script>

<section id="skills">
  <h2>Skills</h2>
  <div class="skill-content">
    <div class="skills-description">
      <p>Some tech-related skill I have learnt and used over the years.</p>
      <p>click on each icon for more details</p>
    </div>
    <div class="skills-icons">
      <div class="skills-grid">
        {#each skills as { name, icon }}
          <div class="skill">
            <i class={icon}></i>
            {name}
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>

<style>
  .skill-content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: flex-start;
    text-align: left;
    /* max-width: 1200px; */
    margin: 0 auto;
    padding: 0 1rem;
    box-sizing: border-box;
  }
  .description h3,
  .skills h3 {
    font-size: 1.5rem;
    margin-bottom: 1rem;
    font-weight: bold;
  }

  .description p {
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
    font-size: 7rem;
    font-weight: bold;
  }

  p {
    font-size: 1.1rem;
    margin-bottom: 2rem 0 0 0;
    line-height: 1.8;
  }

  .about-content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: flex-start;
    text-align: left;
    /* max-width: 1200px; */
    margin: 0 auto;
    padding: 0 1rem;
    box-sizing: border-box;
  }

  .description {
    flex: 1;
    margin-right: 5rem; /* Increase the margin to add more space */
  }

  .software-pic {
    flex: 1;
  }
</style>
