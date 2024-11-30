<script>
  const links = [
    { title: 'Tunebook', url: 'https://tunebook.io/', icon: '', image: '/tunebook.png'},
    { title: 'Tunebook Updates', url: 'https://x.com/TunebookICP', icon: '𝕏'},
    { title: 'LinkedIn', url: 'https://www.linkedin.com/in/robert-ripley-junior/', icon: '', image: '/linkedin.png'},
    { title: 'Twitter Feed', url: 'https://x.com/robvector', icon: '𝕏' },
    { title: 'Spotify', url: 'https://open.spotify.com/artist/0OWHmtLQHNo0CcbmX2V0K8?si=uYw_4V-iQsKT_-OKDmipXQ', icon: '', image: '/spotify.png'},
    { title: 'Soundcloud', url: 'https://soundcloud.com/rob-vector', icon: '', image: '/soundcloud.png'},
    { title: 'Azurescens', url: 'https://open.spotify.com/artist/7fNslsfNHFIc07PPk9aGA6?si=HcNjat9zTzKVFjmBbb37Pw', icon: '', image: '/spotify.png', font: 'Glitch Inside'},
    { title: 'DJ Vector - Psytrance', url: 'https://www.mixcloud.com/robvector/', icon: '👽'},
    { title: 'NFT Art', url: 'https://objkt.com/users/tz1SWXhLLRWRbd3ijqQo3eRT3PXzXBXDtRkW', icon: '', image: '/tezos.png'},
    { title: 'Book a call with Rob', url: 'https://calendly.com/robertripleyjunior/1hour', icon: '☏', isBookCall: true}
  ];
</script>

<svelte:head>
  <title>Rob Vector - Web3 Builder & Artist</title>
</svelte:head>

<main>
  <header>
    <h1>Rob Vector</h1>
    <p>Product Manager<br>
       Web3 Developer<br>
       Electronic Music Producer<br>
       Traditional Celtic Flutist<br>
       NFT Artist</p>
  </header>

  <section class="links">
    {#each links as link}
      <a 
        href={link.url} 
        target="_blank" 
        rel="noopener noreferrer" 
        class={link.isBookCall ? 'book-call' : ''} 
        style="font-family: {link.font ? link.font : 'inherit'}"
      >
        {#if link.image}
          <img src={link.image} alt="{link.title} logo" class="button-image" />
        {/if}
        <span class="icon">{link.icon}</span>
        {link.title}
      </a>
    {/each}
  </section>  
  
</main>

<style>
  /* Add the custom font */
  @font-face {
    font-family: 'Vortax';
    src: url('/fonts/Vortax DEMO.otf') format('truetype');
    font-weight: normal;
    font-style: normal;
  }

  /* Define another custom font, e.g., Lora */
  @font-face {
  font-family: 'Glitch Inside';
  src: url('/fonts/Glitch inside.otf') format('truetype');
  font-weight: normal;
  font-style: normal;
  }
  
  /* Define another custom font, e.g., Lora */
  @font-face {
  font-family: 'Roddenberry';
  src: url('/fonts/Roddenberry.otf') format('truetype');
  font-weight: normal;
  font-style: normal;
  }

  :global(body) {
    margin: 0;
    font-family: 'Roddenberry', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: url('/bg.jpg') no-repeat center center fixed;
    background-size: cover;
    color: white;
    min-height: 100vh;
    font-size: 20px;
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
    font-size: 8rem;
    margin: 0;
    margin-bottom: 1rem;
    text-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
    font-family: 'Vortax', sans-serif; /* Apply the custom font here */
  }

  .links {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* 3 columns */
    gap: 1rem; /* Space between buttons */
    padding: 1rem;
    justify-items: center; /* Centers buttons horizontally */
  }

  .links a {
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    gap: 0.8rem;
    padding: 1rem 1.5rem;
    background: rgba(41, 37, 91, 0.8);
    color: white;
    text-decoration: none;
    border-radius: 0.5rem;
    transition: all 0.2s ease;
    backdrop-filter: blur(5px);
    width: 100%; /* Ensure buttons are consistent width */
    max-width: 300px; /* Limit button width */
}

  .links a.book-call {
    grid-column: 2; /* Center in the second column */
}

  .links a:hover {
    transform: translateY(-2px);
    background: rgba(82, 39, 133, 0.9);
    box-shadow: 0 4px 12px rgba(82, 39, 133, 0.3);
  }

  .icon {
    font-size: 1.5rem;
  }

  .button-image {
  width: 24px; /* Adjust as needed */
  height: 24px; /* Keep it square for consistency */
  margin-right: 8px; /* Add space between the logo and the text */
  vertical-align: middle; /* Align the logo with the text */
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
