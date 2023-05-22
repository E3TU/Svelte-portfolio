<script>
  let test = "hello world";
</script>

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
  <div class="container">
    <h1>Test</h1>
  </div>
</body>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Ubuntu&display=swap');

  $background-color: #191919;
  $foreground-color: #148a55;
  $white: #ffffff;
  $black: #000;

  * {
    margin: 0;
    padding: 0;
  }
  body {
    // display: flex;
    // flex-direction: column;
    margin: 0;
    padding: 0;
    background-color: $background-color;
    font-family: 'Ubuntu', sans-serif;
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
        transition: 1s;
        &:hover{
          color: $background-color;
          transition: 1s;
        }
      }
    }
  }
  .container{
    display: flex;
    align-items: center;
    background-color: #6c0d0d;
    width: calc(100% - 25rem);
    margin-left: 25rem;
    height: 100%;
    // flex: 1;
  }
</style>
