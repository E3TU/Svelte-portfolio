<script>
  let test = "hello world";
</script>

<body>
  <div class="flex-container">
    <div class="navbar">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Skills</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Projects</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </div>
    <div class="container">
      <div class="introduction">
        <img class="profilepic" src="default-profile.png">
        <h1 class="name">E3TU</h1>
        <h1 class="profession">Software Developer</h1>
        <a href="https://github.com/E3TU" class="github-btn">Check My Github</a>
      </div>
    </div>
    <div class="container2">
      
    </div>
  </div>
</body>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Ubuntu&display=swap');
  $background-color: #191919;
  $foreground-color: #148a55;
  $white: #ffffff;
  $black: #000;
  $lighter-gray: #252525;

// Global
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
  font-family: 'Ubuntu', sans-serif;
}

// Page Layout
.flex-container {
  display: flex;
  height: 100vh;
  overflow: hidden;
}

// Side Navigation
.navbar {
  display: flex;
  align-items: center;
  background: $foreground-color;
  // padding-top: 1.5rem;
}

.navbar ul {
  margin: 0;
  padding: 0;
  display: flex;
  list-style: none;
  flex-direction: column;
  font-size: 1.75rem;
}

.navbar ul li a {
  padding: 1rem 10rem;
  font-size: 1.5rem;
  color: $white;
  text-decoration: none;
  display: block;
  transition: 1s;
  &:hover{
   color: $background-color;
   transition: 1s;
  }
}

.container{
  display: flex;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.introduction{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 30rem;
  height: auto;
  margin-bottom: 10rem;
}
.profilepic{
  width: 250px;
  height: 250px;
  border-radius: 50%;
  background-color: $lighter-gray;
}
.name{
  font-size: 3rem;
  color: $foreground-color;
  line-height: 2;
}
.profession{
  font-size: 1.5rem;
  color: $white;
}
.github-btn{
  text-decoration: none;
  color: $white;
  background-color: transparent;
  padding: 15px 45px;
  border-radius: 6px;
  font-size: 1.2rem;
  margin-top: 2rem;
  border: 2px solid $foreground-color;
  transition: 0.7s;
  &:hover{
    background-color: $foreground-color;
    transition: 0.7s;
  }
}
</style>