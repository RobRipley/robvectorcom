<script>
  const links = [
    { title: '𝕏 Personal', url: 'https://x.com/robvector', icon: '🐦' },
    { title: 'Solo Music', url: 'https://open.spotify.com/artist/0OWHmtLQHNo0CcbmX2V0K8?si=uYw_4V-iQsKT_-OKDmipXQ', icon: '🎵' },
    { title: 'Collaborative EP', url: 'https://open.spotify.com/artist/7fNslsfNHFIc07PPk9aGA6?si=HcNjat9zTzKVFjmBbb37Pw', icon: '🎧' },
    { title: 'DJ Sets', url: 'https://www.mixcloud.com/robvector/', icon: '🎹' },
    { title: 'Digital Art', url: 'https://objkt.com/users/tz1SWXhLLRWRbd3ijqQo3eRT3PXzXBXDtRkW', icon: '🎨' },
    { title: 'LinkedIn', url: 'https://www.linkedin.com/in/robert-ripley-junior/', icon: '💼' },
    { title: 'Tunebook', url: 'https://tunebook.io/', icon: '🪕' },
    { title: 'Tunebook Updates', url: 'https://x.com/TunebookICP', icon: '📯' }
  ];
</script>

<svelte:head>
  <title>Rob Vector - Digital Artist & Developer</title>
</svelte:head>

<main>
  <header>
    <h1>Rob Vector</h1>
    <p>Electronic Music Producer • Digital Artist • Developer</p>
  </header>

  <section class="links">
    {#each links as link}
      <a href={link.url} target="_blank" rel="noopener noreferrer">
        <span class="icon">{link.icon}</span>
        {link.title}
      </a>
    {/each}
  </section>
</main>

<style>
  :global(body) {
    margin: 0;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: url('/bg.jpg') no-repeat center center fixed;
    background-size: cover;
    color: white;
    min-height: 100vh;
  }

  main {
    max-width: 1200px;
    margin: 0 auto;
    padding: 2rem;
    background: rgba(0, 0, 0, 0.5);
    min-height: 100vh;
    backdrop-filter: blur(5px);
  }

  header {
    text-align: center;
    padding: 4rem 0;
    background: rgba(41, 37, 91, 0.7);
    color: white;
    border-radius: 1rem;
    margin-bottom: 3rem;
    backdrop-filter: blur(10px);
  }

  h1 {
    font-size: 3rem;
    margin: 0;
    margin-bottom: 1rem;
    text-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
  }

  .links {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1rem;
    padding: 1rem;
  }

  .links a {
    display: flex;
    align-items: center;
    gap: 0.8rem;
    padding: 1rem 1.5rem;
    background: rgba(41, 37, 91, 0.8);
    color: white;
    text-decoration: none;
    border-radius: 0.5rem;
    transition: all 0.2s ease;
    backdrop-filter: blur(5px);
  }

  .links a:hover {
    transform: translateY(-2px);
    background: rgba(82, 39, 133, 0.9);
    box-shadow: 0 4px 12px rgba(82, 39, 133, 0.3);
  }

  .icon {
    font-size: 1.5rem;
  }

  @media (max-width: 768px) {
    h1 {
      font-size: 2rem;
    }
    
    .links {
      grid-template-columns: 1fr;
    }
  }
</style>