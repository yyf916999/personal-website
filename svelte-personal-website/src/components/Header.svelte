<script>
  import { onMount } from "svelte";
  let name = "Yufan Yang";
  let tagline = "Yufan Yang";
  let names = [
    "I am a Full-Stack Software Developer",
    "I Turn Ideas Into Reality",
  ];
  let currentNameIndex = 0;
  let currentName = "";
  let typing = true;
  function typeWriterEffect() {
    if (typing) {
      if (currentName.length < names[currentNameIndex].length) {
        currentName += names[currentNameIndex][currentName.length];
        setTimeout(typeWriterEffect, 50); // Typing speed
      } else {
        typing = false;
        setTimeout(typeWriterEffect, 1500); // Pause before deleting
      }
    } else {
      if (currentName.length > 0) {
        currentName = currentName.slice(0, -1);
        setTimeout(typeWriterEffect, 50); // Deleting speed
      } else {
        typing = true;
        currentNameIndex = (currentNameIndex + 1) % names.length;
        setTimeout(typeWriterEffect, 500); // Pause before typing next name
      }
    }
  }
  onMount(() => {
    typeWriterEffect();
  });
</script>

<header>
  <nav>
    <div class="logo">
      <img id="letter-y" src="/assets/letter-y.png" />{tagline}
    </div>
    <div class="nav-links">
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#contacts">Contacts</a>
      <a href="#resume">Resume</a>
    </div>
  </nav>

  <div class="hero">
    <div class="hero-text">
      <h1>{name}</h1>
      <p class="tagline">{currentName}</p>
      <a
        class="resume-button"
        href="/assets/Yufan-Yang-Software Engineer.pdf"
        download>Download Resume</a
      >
    </div>
    <div class="hero-image">
      <img src="/assets/pfp.png" alt={name} />
    </div>
  </div>
</header>

<style>
  header {
    /* background: url("/assets/header-background.jpg") no-repeat center center; */
    /* background-color: #f0f0f0; */
    background: white;
    background-size: cover;
    color: white;
    text-align: center;
    padding: 2rem;
    position: relative;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  nav {
    width: 100%;
    box-sizing: border-box;
    padding: 2rem 10rem 1rem 10rem;
    display: flex;
    justify-content: space-between;
    position: absolute;
    top: 0;
    left: 0;
    background: white;
  }
  nav:after {
    position: absolute;
    content: "";
    border-bottom: 1px solid black;
    width: 90%;
    transform: translateX(-50%);
    bottom: 0px;
    left: 50%;
  }
  .logo {
    display: flex;
    font-size: 1.5rem;
    font-weight: bold;
    color: black;
    gap: 0.5rem;
  }
  #letter-y {
    max-width: 1.5rem;
    max-height: 2rem;
  }

  .nav-links {
    display: flex;
    gap: 1rem;
  }

  .nav-links a {
    color: black;
    text-decoration: none;
    font-size: 1rem;
    font-weight: 700;
  }

  .hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    max-width: 1200px;
    margin-top: 5rem; /* Adjust as needed */
  }

  .hero-text {
    max-width: 50%;
    text-align: left;
    color: black;
  }

  .hero h1 {
    font-size: 3rem;
    margin: 0.5rem 0;
  }

  .tagline {
    font-size: 1.5rem;
    margin: 0.5rem 0 2rem 0;
    min-height: 1.5em;
  }

  /* .contact-button {
    padding: 0.75rem 1.5rem;
    background-color: #f04e4e;
    border: none;
    border-radius: 5px;
    color: white;
    font-size: 1rem;
    cursor: pointer;
  }

  .contact-button:hover {
    background-color: #d43d3d;
  } */

  .hero-image img {
    /* max-width: 500px; */
    border-radius: 10px;
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
</style>
