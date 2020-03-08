<script>
  export let title;
  export let img;
  export let description;
  export let url;
  export let contacts;
  export let slug;
</script>

<div class="card">
  <div class="card-image">
    <figure class="image">
      <img src={"img/groups/"}{img} alt="Placeholder image">
    </figure>
  </div>
  <div class="card-content">
    <p class="title is-5">{title}</p>
    <div class="content">
      {description}

      <ul>
        <li><a href={url} target="_blank">Sito</a></li>
        {#if contacts}
          {#each contacts as contact}
            <li><a href={contact.url} target="_blank">{contact.label}</a></li>
          {/each}
        {/if}
      </ul>

    </div>
  </div>
  <footer class="card-footer">
    <a href={"groups/"}{slug} class="card-footer-item">Eventi</a>
  </footer>
</div>
