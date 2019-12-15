<script>
  let loggedIn = false;

  function signUp(event) {
    event.preventDefault();
    loggedIn = true;
  }
  function logIn(event) {
    event.preventDefault();
    loggedIn = true;
  }
  function logOut(event) {
    event.preventDefault();
    loggedIn = false;
  }
</script>

<nav>
  <form>
    {#if !loggedIn}
      <label for="username">
        <span>username:</span>
        <input id="username" type="text" />
      </label>
      <label for="password">
        <span>password:</span>
        <input id="password" type="password" />
      </label>
      <button type="submit" on:click={signUp}>sign up</button>
      <button type="submit" on:click={logIn}>login</button>
    {:else}
      <button type="submit" on:click={logOut}>logout</button>
    {/if}
  </form>
</nav>
