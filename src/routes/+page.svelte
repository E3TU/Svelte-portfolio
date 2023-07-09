<script>
  import Navbar from "./Navbar.svelte";
  // import Fa from "svelte-fa";
  // import { faJs } from "@fortawesome/free-brands-svg-icons";
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
    <div class="aboutme">
      <p>
        Hello &#x1F44B;, My name is Eetu, I am a passionate software developer
        currently studying in the field. I am interested in web and Android
        development and also Linux. In my free time i like to code and exercise.
        I have built multiple websites/apps and also some android apps.
      </p>
      <h3>Experience</h3>
      <p class="experiencetext">
        I have about 2-years of experience in Software Development field. I have
        done different kinds of projects on my free time, learned some coding at
        school and also had two interships in software companies. Most of my
        coding knowledge is from interships and making my own projects in free
        time.
      </p>
    </div>
  </div>

  <div id="skills" class="container">
    <h4>Why to choose me</h4>
    <h1>Skills</h1>
    <div class="myskills">
      <div class="box">
        <h1>Web</h1>
        <p>Html, Css, Javascript, Scss</p>
        <p>NodeJs, Svelte, Express</p>
        <p>MongoDB, MySQL</p>
      </div>
      <div class="box">
        <h1>Mobile</h1>
        <p>Android, Kotlin</p>
      </div>
      <div class="box">
        <h1>Other</h1>
        <p>Linux, Bash</p>
        <p>C#</p>
      </div>
    </div>
  </div>

  <div id="projects" class="container">
    <h4>My work</h4>
    <h1>Projects</h1>
    <div class="flexcontainer">
      <div class="project">
        <h1>Android password generator</h1>
        <p>
          Simple password generator app made for Android using Kotlin. The app
          has simple gui and adjustable password length.
        </p>
        <a
          class="github-link"
          href="https://github.com/E3TU/Android-passwordgen">Github</a
        >
      </div>
      <div class="project">
        <h1>Javascript Todo App</h1>
        <p>
          Todo app made with VanillaJS. Uses localstorage to save the tasks.
          Tasks can be deleted and edited.
        </p>
        <a class="github-link" href="https://github.com/E3TU/TodoApp">Github</a>
      </div>
      <div class="project">
        <h1>Javascript Clock App</h1>
        <p>
          Clock app made with VanillaJS. Has both analog and digital clock as
          well as dark and light modes.
        </p>
        <a class="github-link" href="https://github.com/E3TU/clock">Github</a>
      </div>
      <div class="project">
        <h1>Under work...</h1>
      </div>
    </div>
  </div>

  <div id="contact" class="container">
    <h4>Get in touch</h4>
    <h1>Contact</h1>
    <div class="contactcontainer">
      <form
        class="contactform"
        name="contactform"
        method="POST"
        data-netlify="true"
      >
        <div class="labelcontainer">
          <p>
            <label>Name<input type="text" name="name" class="name" /></label>
          </p>
        </div>
        <div class="labelcontainer">
          <p>
            <label>Email<input type="email" name="email" /></label>
          </p>
        </div>
        <div class="labelcontainer">
          <p>
            <label>Message<textarea name="message" /></label>
          </p>
        </div>
        <br />
        <div class="labelcontainer">
          <p>
            <button id="submit" type="submit">Send</button>
          </p>
        </div>
      </form>
    </div>
  </div>
</body>

<style lang="scss">
  @import url("https://fonts.googleapis.com/css2?family=Ubuntu&display=swap");
  $background-color: #191919;
  $foreground-color: #148a55;
  $white: #ffffff;
  $black: #000;
  $lighter-gray: #252525;
  $rounded-border: 6px;

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
  #home-container {
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
    border-radius: $rounded-border;
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
    h4 {
      margin-top: 2rem;
      color: $foreground-color;
    }
  }
  #about {
    height: 100vh !important;
  }
  .aboutme {
    height: auto;
    width: 40rem;
    margin-top: 2rem;
    font-size: 1.25rem;
    p {
      color: $white;
    }
    h3 {
      margin-top: 1rem;
      color: $foreground-color;
    }
    .experiencetext {
      margin-top: 1rem;
    }
  }

  .myskills {
    display: flex;
    gap: 2rem;
    h1 {
      margin-left: 1rem;
      font-size: 2rem;
    }
    p {
      color: $foreground-color;
      margin-left: 1rem;
      margin-top: 1rem;
      font-weight: bold;
    }
  }
  .box {
    margin-top: 5rem;
    width: 20rem;
    height: 22rem;
    background-color: $background-color;
    box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px,
      rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px,
      rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
    border-radius: $rounded-border;
  }
  .flexcontainer {
    margin-top: 4rem;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    gap: 2rem;
    width: 70rem;
  }
  .project {
    display: flex;
    flex-direction: column;
    height: 15rem;
    width: 30rem;
    background-color: $background-color;
    box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px,
      rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px,
      rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
    border-radius: $rounded-border;
    h1 {
      font-size: 1.5rem;
      margin-left: 1rem;
      color: $foreground-color;
    }
    p {
      margin-left: 1.2rem;
      margin-top: 1rem;
      color: $white;
      line-height: 1.25;
      flex: 1;
      width: 25rem;
    }
  }
  .github-link {
    text-decoration: none;
    color: $white;
    padding: 10px 24px;
    background-color: transparent;
    border-radius: $rounded-border;
    max-width: min-content;
    margin-left: 1rem;
    margin-bottom: 1rem;
    border: 2px solid $foreground-color;
    transition: 0.5s;
    &:hover {
      background-color: $foreground-color;
      transition: 0.5s;
    }
  }
  .contactcontainer {
    display: flex;
    height: auto;
    width: 30rem;
    justify-content: center;
    h3 {
      color: $foreground-color;
      margin-top: 1rem;
    }
  }
  .contactform {
    position: relative;
    margin-top: 6rem;
    color: #fff;
    width: 26rem;
    height: auto;
    p {
      font-size: 3rem;
    }
  }
  .contactform input {
    height: 3rem;
    font-size: 1.5rem;
    display: block;
    margin: auto;
    width: 100%;
    background-color: #fff;
    border: none;
    color: #000;
    font-family: "Poppins", sans-serif;
    padding-left: 0.2rem;
  }
  .contactform textarea {
    height: 6rem;
    font-size: 1.5rem;
    display: block;
    margin: auto;
    width: 100%;
    background-color: #fff;
    border: none;
    color: #000;
    font-family: "Poppins", sans-serif;
    padding-left: 0.2rem;
  }
  .labelcontainer {
    width: 25rem;
    text-align: left;
    margin: auto;
  }
  #submit {
    text-decoration: none;
    color: $white;
    padding: 12px 24px;
    background-color: transparent;
    border: 2px solid $foreground-color;
    border-radius: $rounded-border;
    font-size: 1rem;
    transition: 0.5s;
    &:hover{
      background-color: $foreground-color;
      transition: 0.5s;
    }
  }
  @media only screen and (max-width: 1499px) {
    #home-container{

    }
    // .container{
    //   // justify-content: center;
    //   align-items: center;
    //   margin-left: 0;
    //   width: 100%;
    // }
    .flexcontainer{
      width: 60rem;
    }
    .project{
      width: 25rem;
    }
    .box{
      width: 18rem;
    }
  }
  @media only screen and (max-width: 1360px) {
    .box{
      width: 16rem;
    }
  }
  @media only screen and (max-width: 1320px) {
    .flexcontainer{
      width: 50rem;
    }
    .project{
      width: 40rem;
    }
    #contact{
      margin-top: 25rem;
    }
  }
  @media only screen and (max-width: 1259px) {
    .myskills{
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
      width: 30rem;
    }
    .box{
      margin-top: 2rem;
      width: 30rem;
      height: 15rem;
    }
    #projects{
      margin-top: 10rem;
    }
  }
</style>
