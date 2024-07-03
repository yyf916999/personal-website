<section>
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
</section>

<style>
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
</style>
