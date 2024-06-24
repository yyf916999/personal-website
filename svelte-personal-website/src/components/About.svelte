<script>
  let skills = [
    "HTML",
    "CSS",
    "JavaScript",
    "React",
    "WordPress",
    "PHP",
    "SASS",
    "GIT",
    "Github",
    "Responsive Design",
    "SEO",
    "Terminal",
  ];
</script>

<section id="about">
  <h2>ABOUT ME</h2>
  <p>
    Here you will find more information about me, what I do, and my current
    skills mostly in terms of programming and technology.
  </p>

  <div class="about-content">
    <div class="description">
      <h3>Get to know me!</h3>
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
        {#each skills as skill}
          <span class="skill">{skill}</span>
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
    background-color: #e0e0e0;
    padding: 0.5rem 1rem;
    border-radius: 5px;
    font-size: 0.9rem;
  }

  a {
    color: #007bff;
    text-decoration: none;
  }

  a:hover {
    text-decoration: underline;
  }
</style>
