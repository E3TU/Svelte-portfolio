<script>
  let test = "hello world";
</script>

<svelte:head>
  <link
    href="https://fonts.googleapis.com/css2?family=Poppins&display=swap"
    rel="stylesheet"
  />
</svelte:head>

<body>
  <header class="navbar">
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About me</a></li>
        <li><a href="#">Skills</a></li>
        <li><a href="#">Projects</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>
</body>

<style lang="scss">
  @import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");

  $background-color: #191919;
  $foreground-color: #148a55;
  $white: #ffffff;

  * {
    margin: 0;
    padding: 0;
  }

  body {
    margin: 0;
    padding: 0;
    background-color: $background-color;
    font-family: "Poppins", sans-serif;
  }
  .navbar {
    display: flex;
    position: fixed;
    height: 100%;
    width: 25rem;
    background-color: #148a55;
    align-items: center;
    justify-content: flex-start;
  }
  ul {
    display: flex;
    list-style: none;
     flex-direction: column;
    font-size: 1.75rem;
    margin-left: 5rem;

    li {
      padding: 1rem;

      a {
        text-decoration: none;
        color: $white;
      }
    }
  }
</style>
