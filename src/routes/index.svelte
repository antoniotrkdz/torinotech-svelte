<script>
  import Card from "../components/Card.svelte"
  import groups from "../../data/groups.json"
</script>

<style>
	h1, figure, p {
		text-align: center;
		margin: 0 auto;
	}

	h1 {
		font-size: 2.8em;
		text-transform: uppercase;
		font-weight: 700;
		margin: 0 0 0.5em 0;
	}

	figure {
		margin: 0 0 1em 0;
	}

	img {
		width: 100%;
		max-width: 400px;
		margin: 0 0 1em 0;
	}

	p {
		margin: 1em auto;
	}

	@media (min-width: 480px) {
		h1 {
			font-size: 4em;
		}
	}
</style>

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
