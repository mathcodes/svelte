<script>
  let firstName = "Jon";
  let lastName = "Christie";
	let bio = "• Web Developer • Educator"
  let color = "purple"
  let showText = false
  let users = [
    {
      id: '1',
      name: 'Jonathan'
    },
    {
      id: '2',
      name: 'Joanne'
    },
    {
      id: '3',
      name: 'Nathan'
    },
  ]
  $: name = firstName + ' ' + lastName + ' ' + bio
 

  function getRandomItem(arr) {
    // get random index value
    const randomIndex = Math.floor(Math.random() * arr.length);

    // get random item
    const item = arr[randomIndex];

    return item;
  }

  const array = [
    "red",
    "orange",
    "yellow",
    "green",
    "blue",
    "indigo",
    "violet",
  ];

  const toggle = () => {
    console.log(name)
    color =	 getRandomItem(array);
    showText = !showText 
    users = [...users, { id: '4', name: 'Jen'}]
  };
  console.log(name)
 
</script>

 
<!-- OUTPUT / HTML  -->
<main>
  
  <h1 style="color: {color}">Hello {name}!</h1>
  {#if showText}
    <p>Visit our site!</p>
    {:else}
    <p>No Text</p>
  {/if}

  <!-- <button on:click={()=> color = 'purple'}>CLICK ME </button> -->
  <button on:click={toggle}>CLICK ME </button>

  {#each users as user (user.id)}
    <h3>{user.id}: {user.name}</h3>
  {/each}
</main>

<!-- STYLE TAGS  -->
<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
