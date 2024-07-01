<script>
  import Header from "./components/Header.svelte";
  import About from "./components/About.svelte";
  import Contact from "./components/Contact.svelte";
  import Resume from "./components/Resume.svelte";
  import Videos from "./components/Video.svelte";
</script>

<main>
  <Header name="Yufan Yang" />
  <About />
  <Resume />
  <Videos />
  <Contact />
</main>

<style>
  main {
    font-family: Arial, sans-serif;
  }
</style>
