<script>
  // Array to hold video URLs
  let videos = [
    {
      title: "This was my last dance in college",
      url: "https://www.youtube.com/embed/0ILpDTXTmHM",
    },
    {
      title: "Turn down your volume",
      url: "/assets/nathan.mp4",
    },
    {
      title: "Gaming Highlights",
      url: "https://www.youtube.com/watch?v=I5lq6sCuABE&ab_channel=theroadmap",
    },
  ];
</script>

<section id="videos">
  <h2>Just some videos about my hobbies</h2>
  {#each videos as { title, url }}
    <div class="video-container">
      <h3>{title}</h3>
      <iframe
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
    background-color: #f0f0f0;
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
