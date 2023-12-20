<script>
  let name = "E3TU";
</script>

<svelte:head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>E3TU's portfolio</title>
</svelte:head>

<body>
  <div class="flexbox">
    <h1>{name}</h1>
    <div class="terminal">
      <div class="titlebar">
        <div class="buttons">
          <button id="minimize" class="window-button" />
          <button id="maximize" class="window-button" />
          <button id="close" class="window-button" />
        </div>
      </div>
      <div class="introduction">
        <h3>{name}:~$ <span class="whitetext">introduction</span></h3>
        <h4>Hello👋, I'm Eetu, Software developer from Finland</h4>
      </div>
      <div class="about">
        <h3>{name}:~$ <span class="whitetext">about me</span></h3>
        <div class="aboutmetext">
          <h4>
            My name is Eetu, I am a passionate software developer currently
            studying in the field. I am interested in web and Android
            development and also Linux. In my free time i like to code and
            exercise. I have built multiple websites&webapps and also some
            android apps.
          </h4>
        </div>
      </div>
      <div class="skills">
        <h3>{name}:~$ <span class="whitetext">skills</span></h3>
        <div class="flex-item">
          <h4>Web</h4>
          <h5>Html</h5>
          <h5>Css</h5>
          <h5>Javascript</h5>
          <h5>NodeJs</h5>
          <h5>Svelte</h5>
        </div>
        <div class="flex-item">
          <h4>Mobile</h4>
          <h5>Android</h5>
          <h5>Kotlin</h5>
        </div>
        <div class="flex-item">
          <h4>Other</h4>
          <h5>C#</h5>
          <h5>Linux</h5>
          <h5>Bash</h5>
        </div>
      </div>
      <div class="projects">
        <h3>{name}:~$ <span class="whitetext">projects</span></h3>
        <div class="project-item">
          <h4>Android password generator</h4>
          <a href="https://github.com/E3TU/Android-passwordgen">GitHub</a>
        </div>
        <div class="project-item">
          <h4>Javascript todo app</h4>
          <a href="https://github.com/E3TU/TodoApp">GitHub</a>
        </div>
        <div class="project-item">
          <h4>Javascript clock app</h4>
          <a href="https://github.com/E3TU/clock">GitHub</a>
        </div>
        <div class="project-item">
          <h4>Bash random password generator</h4>
          <a href="https://github.com/E3TU/Bash-random-password-generator">GitHub</a>
        </div>
      </div>
      <div class="contact">
        <h3>{name}:~$ <span class="whitetext">Contact</span></h3>
        <h4>You can contact me via my email alias: <a href="mailto:e3tu.1bhe3@slmail.me">e3tu.1bhe3@slmail.me</a></h4>
      </div>
      <div class="end">
        <h3>{name}:~$ <span class="whitetext"></span></h3>
      </div>
    </div>
  </div>
</body>

<style lang="scss">
  @import url("https://fonts.googleapis.com/css2?family=Ubuntu&display=swap");

  * {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
    font-family: "Ubuntu", sans-serif;
  }
  body {
    padding: 0;
    margin: 0;
    background-color: $background-color;
    font-family: "Ubuntu", sans-serif;
    letter-spacing: 0.05rem;
  }
  .flexbox {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    h1 {
      margin-top: 3rem;
      color: $foreground-color;
      position: relative; /* Set position to relative to allow cursor positioning */
      display: inline-block; /* To make the cursor pseudo-element inline */
      text-shadow: 1px 1px $black;
      &::after {
        content: "▌"; /* Cursor content */
        position: absolute;
        bottom: 0;
        left: 100%; /* Position cursor after the "User" text */
        animation: blink 1s infinite; /* CSS animation for blinking effect */
        color: $foreground-color;
        text-shadow: 1px 1px $black;
      }
    }
  }
  @keyframes blink {
    0%,
    100% {
      opacity: 1; /* Fully visible */
    }
    50% {
      opacity: 0; /* Invisible */
    }
  }
  .terminal {
    background-color: $gray;
    margin-top: 3rem;
    width: 65rem;
    height: 47rem;
    border-radius: 10px;
    box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px,
      rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px,
      rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
    h3 {
      color: $foreground-color;
      margin-top: 1rem;
      margin-left: 1rem;
      font-size: 1.5rem;
    }
    h4 {
      color: $white;
      margin-top: 1rem;
      margin-left: 1rem;
      font-size: 1rem;
    }
    h5 {
      color: $white;
      margin-top: 1rem;
      margin-left: 1rem;
    }
  }
  .titlebar {
    display: flex;
    justify-content: center;
    background-color: $black;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    width: 100%;
    height: 2rem;
    flex-direction: column;
    align-items: flex-end;
  }
  .buttons {
    margin-right: 1rem;
  }
  .window-button {
    width: 0.8rem;
    height: 0.8rem;
    border: none;
    border-radius: 50%;
    &:hover {
      opacity: 0.8;
    }
  }
  #close {
    background-color: $red;
  }
  #maximize {
    background-color: $yellow;
  }
  #minimize {
    background-color: $green;
  }
  .whitetext {
    color: $white;
  }
  .aboutmetext {
    width: 60%;
    line-height: 1.5;
    // letter-spacing: 0.05rem;
  }
  .skills {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    h3{
      width: 100%;
    }
    h5 {
      margin-top: 0.5rem !important;
    }
  }
  .flex-item{
    width: 8rem;
  }
  .projects{
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    h3{
      width: 100%;
    }
    h4{
      margin-left: 1rem;
      color: $foreground-color;
    }
    a{
      margin-left: 1rem;
      background-color: transparent;
      color: $white;
      font-size: 0.8rem;
    }
  }
  .project-item{
    width: auto;
  }
  .contact{
    a{
      color: $foreground-color;
    }
  }
  @media only screen and (max-width: 1076px) {
    .terminal{
      width: 50rem;
    }
  }
  @media only screen and (max-width: 850px) {
    .terminal{
      width: 40rem;
    }
    .end{
      display: none;
    }
  }
  @media only screen and (max-width: 680px) {
    .terminal{
      width: 30rem;
      height: auto;
      padding-bottom: 2rem;
      margin-bottom: 2rem;
      h3{
        font-size: 1rem;
      }
      h4{
        font-size: 0.9rem;
      }
    }
  }
  @media only screen and (max-width: 525px) {
    .terminal{
      width: 25rem;
      margin-bottom: 1rem;
    }
    .flexbox{
      h1{
        margin-top: 1.6rem;
      }
    }
  }
  @media only screen and (max-width: 440px) {
    .terminal{
      width: 22rem;
    }
  }
  @media only screen and (max-width: 380px) {
    .terminal{
      width: 20rem;
    }
  }
</style>
