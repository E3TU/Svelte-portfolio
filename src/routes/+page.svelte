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
        <h5>Hello👋, I'm Eetu, Software developer from Finland</h5>
      </div>
      <div class="about">
        <h3>{name}:~$ <span class="whitetext">about me</span></h3>
        <div class="aboutmetext">
          <h5>My name is Eetu, I am a passionate software developer
            currently studying in the field. I am interested in web and Android
            development and also Linux. In my free time i like to code and exercise.
            I have built multiple websites/apps and also some android apps.
          </h5>
        </div>
      </div>
      <div class="skills">
        <h3>{name}:~$ <span class="whitetext">skills</span></h3>
        <h5></h5>
      </div>
      <div class="projects">

      </div>
      <div class="contact">

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
  }
  body {
    padding: 0;
    margin: 0;
    background-color: $background-color;
    font-family: "Ubuntu", sans-serif;
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
      &::after {
        content: "▌"; /* Cursor content */
        position: absolute;
        bottom: 0;
        left: 100%; /* Position cursor after the "User" text */
        animation: blink 1s infinite; /* CSS animation for blinking effect */
        color: $foreground-color;
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
    background-color: $background-color;
    margin-top: 3rem;
    width: 60rem;
    height: 45rem;
    border-radius: 10px;
    box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px,
      rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px,
      rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
      h3{
        color: $foreground-color;
        margin-top: 1rem;
        margin-left: 1rem;
      }
      h5{
        color: $white;
        margin-top: 1rem;
        margin-left: 1rem;
      }
  }
  .titlebar {
    display: flex;
    justify-content: center;
    background-color: #101010;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    width: 100%;
    height: 2rem;
    flex-direction: column;
    align-items: flex-end;
  }
  .buttons{
    margin-right: 1rem;
  }
  .window-button {
    width: .80rem;
    height: .80rem;
    border: none;
    border-radius: 50%;
    &:hover{
      opacity: 0.8;
    }
  }
  #close{
    background-color: $red;
  }
  #maximize{
    background-color: $yellow;
  }
  #minimize{
    background-color: $green;
  }
  .home{
    width: 100%;
    height: auto;
  }
  .whitetext{
    color: $white;
  }
  .aboutmetext{
    width: 60%;
    line-height: 1.5;
    letter-spacing: 0.05rem;
  }
</style>
