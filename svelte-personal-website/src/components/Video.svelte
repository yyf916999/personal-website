<script>
  // Array to hold video URLs
  let videos = [
    {
      title: "This was my last dance in college",
      url: "https://www.youtube.com/embed/0ILpDTXTmHM",
    },
    {
      title: "I want to learn this next",
      url: "https://www.youtube.com/embed/OMcOAkoa8oM",
    },
  ];
</script>

<section id="videos">
  <h2>Just some videos about my hobbies</h2>
  {#each videos as { title, url }}
    <div class="video-container">
      <h3>{title}</h3>
      <iframe
        title="video"
        src={url}
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      >
      </iframe>
    </div>
  {/each}
</section>

<style>
  #videos {
    padding: 2rem;
    background: white;
    text-align: center;
  }

  .video-container {
    margin: 1rem auto;
    max-width: 560px;
  }

  iframe {
    width: 100%;
    height: 315px;
  }

  h3 {
    margin: 0.5rem 0;
  }
</style>
