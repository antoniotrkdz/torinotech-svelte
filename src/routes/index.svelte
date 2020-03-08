<script>
  import Card from "../components/Card.svelte"
  import { groups } from "../../data/groups.json"
</script>

<svelte:head>
	<title>Sapper project template</title>
</svelte:head>

<div class="section">
  <div class="container">
    <h1 class="title"><a href="/">Torino Tech</a></h1>
  </div>
</div>

<section class="section">
  <div class="container">
    <b>Groups</b>
      <div class="columns is-multiline">
        {#each groups as group}
        <div class="column is-one-quarter">
          <Card {...group} />
        </div>
      {/each}
    </div>
  </div>
</section>
