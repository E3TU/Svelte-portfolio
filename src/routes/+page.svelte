<script>
  import Navbar from "./Navbar.svelte";
</script>

<body>
  <Navbar />

  <div id="home-container">
    <div class="introduction">
      <img class="profilepic" src="default-profile.png" />
      <h1 class="name">E3TU</h1>
      <h1 class="profession">Software Developer</h1>
      <a href="https://github.com/E3TU" class="github-btn">Check My Github</a>
    </div>
  </div>

  <div id="about" class="container">
    <h4>Info about me</h4>
    <h1>About Me</h1>
  </div>

  <div id="skills" class="container">
    <h4>Why to choose me</h4>
    <h1>Skills</h1>
  </div>

  <div id="projects" class="container">
    <h4>My work</h4>
    <h1>Projects</h1>
  </div>

  <div id="contact" class="container">
    <h4>Get in touch</h4>
    <h1>Contact</h1>
  </div>
</body>

<style lang="scss">
  @import url("https://fonts.googleapis.com/css2?family=Ubuntu&display=swap");
  $background-color: #191919;
  $foreground-color: #148a55;
  $white: #ffffff;
  $black: #000;
  $lighter-gray: #252525;


  * {
    font-family: sans-serif;
    box-sizing: border-box;
    padding: 0;
    margin: 0;
  }

  body {
    padding: 0;
    margin: 0;
    background-color: $background-color;
    font-family: "Ubuntu", sans-serif;
  }
  #home-container{
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    width: calc(100% - 25rem);
    margin-left: 25rem;
    flex: 1;
  }
  .introduction {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 30rem;
    height: auto;
    margin-bottom: 10rem;
  }
  .profilepic {
    width: 250px;
    height: 250px;
    border-radius: 50%;
    background-color: $lighter-gray;
  }
  .name {
    font-size: 3rem;
    color: $foreground-color;
    line-height: 2;
  }
  .profession {
    font-size: 1.5rem;
    color: $white;
  }
  .github-btn {
    text-decoration: none;
    color: $white;
    background-color: transparent;
    padding: 15px 45px;
    border-radius: 6px;
    font-size: 1.2rem;
    margin-top: 2rem;
    border: 2px solid $foreground-color;
    transition: 0.7s;
    &:hover {
      background-color: $foreground-color;
      transition: 0.7s;
    }
  }
  .container {
    display: flex;
    align-items: center;
    flex-direction: column;
    height: 100vh;
    width: calc(100% - 25rem);
    margin-left: 25rem;
    flex: 1;
    h1 {
      color: $white;
      margin-top: 1rem;
      font-size: 3rem;
    }
    h4{
      margin-top: 2rem;
      color: $foreground-color;
    }
  }
</style>
