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
  ];
</script>

<section id="about">
  <h2>ABOUT ME</h2>

  <div class="about-content">
    <div class="description">
      <p>
        I'm a <strong>Frontend Focused Web Developer</strong> building and managing
        the Front-end of Websites and Web Applications that leads to the success
        of the overall product. Check out some of my work in the Projects section.
      </p>
      <p>
        I also like sharing content related to the stuff that I have learned
        over the years in <strong>Web Development</strong> so it can help other
        people of the Dev Community. Feel free to Connect or Follow me on my
        <a href="#">LinkedIn</a>
        and <a href="#">Instagram</a> where I post useful content related to Web
        Development and Programming.
      </p>
      <p>
        I'm open to <strong>Job</strong> opportunities where I can contribute,
        learn, and grow. If you have a good opportunity that matches my skills
        and experience, then don't hesitate to <strong>contact</strong> me.
      </p>
    </div>
    <div class="skills">
      <h3>My Skills</h3>
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
  section {
    padding: 2rem 1rem;
    background-color: #f9f9f9;
  }

  h2 {
    text-align: center;
    margin-bottom: 1rem;
    font-size: 2rem;
    font-weight: bold;
  }

  p {
    text-align: center;
    font-size: 1.1rem;
    margin-bottom: 2rem;
  }

  .about-content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: flex-start;
    text-align: left;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1rem;
    box-sizing: border-box;
  }

  .description {
    flex: 1;
    margin-right: 5rem; /* Increase the margin to add more space */
  }

  .skills {
    flex: 1;
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

  a {
    color: #007bff;
    text-decoration: none;
  }

  a:hover {
    text-decoration: underline;
  }
</style>
