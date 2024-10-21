<script lang="ts">
  import { writable } from "svelte/store";
  export let count = writable(0);
  let username: string = "";
  let password: string = "";

  const handleClick = () => {
    count.update((n) => n + 1);
  };

  const handleLogin = (e: Event) => {
    e.preventDefault();
    const data = { username, password };

    console.log("info", data);

    console.log("login");
  };
  $: {
    console.log("Writable", writable);
  }
</script>

<section>
  <h1 class="text-red-300">Blog Page</h1>
  <h2>
    Lorem ipsum dolor, sit amet consectetur adipisicing elit. Inventore deserunt
    sit, unde nobis sequi repellat fugit ipsam iusto modi molestiae totam
    corrupti reprehenderit animi nesciunt, cumque deleniti expedita pariatur
    necessitatibus?
  </h2>

  <button class="bg-blue-300 rounded-full px-2 py-3" on:click={handleClick}
    >Clicked {$count}
  </button>

  <form action="" on:submit={handleLogin}>
    <input type="text" placeholder="username" bind:value={username} />
    <input type="text" placeholder="password" bind:value={password} />
    <button>Login</button>
  </form>
</section>
