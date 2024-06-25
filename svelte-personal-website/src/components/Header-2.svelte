<script>
  import { onMount } from "svelte";

  let names = ["Hi, I am Yufan Yang", "I Turn Ideas Into Reality"];
  let currentNameIndex = 0;
  let currentName = "";
  let typing = true;

  function typeWriterEffect() {
    if (typing) {
      if (currentName.length < names[currentNameIndex].length) {
        currentName += names[currentNameIndex][currentName.length];
        setTimeout(typeWriterEffect, 150); // Typing speed
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
  <h1>{currentName}</h1>
  <nav>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<style>
  header {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 2rem;
    color: #fff;
    background-color: green;
    /* background-image: url("/assets/header-background.jpg"); */
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    min-height: 300px; /* Adjust the height as needed */
  }

  h1 {
    margin: 0;
    padding: 0;
    text-align: center;
    min-height: 1.5em; /* Ensure space is reserved for text */
  }

  nav {
    margin-top: 1rem;
  }

  nav a {
    margin: 0 1rem;
    color: #fff;
    text-decoration: none;
  }
</style>
