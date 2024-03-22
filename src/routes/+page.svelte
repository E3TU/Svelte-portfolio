<script>
  import { name } from "../store/store";

  // Import components
  import Introduction from "../components/Introduction.svelte";
  import About from "../components/About.svelte";
  import Skills from "../components/Skills.svelte";
  import Projects from "../components/Projects.svelte";
  import Contact from "../components/Contact.svelte";
  import BottomSection from "../components/BottomSection.svelte";
</script>

<svelte:head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>E3TU's portfolio</title>
</svelte:head>

<body>
  <div class="flexbox">
    <h1>{$name}</h1>
    <div class="terminal">
      <div class="titlebar">
        <div class="buttons">
          <button id="minimize" class="window-button" />
          <button id="maximize" class="window-button" />
          <button id="close" class="window-button" />
        </div>
      </div>
      <!--Components-->
      <Introduction />
      <About />
      <Skills />
      <Projects />
      <Contact />
      <BottomSection />
    </div>
  </div>
</body>

<style lang="scss">

  body {
    padding: 0;
    margin: 0;
    background: url("/gradient.svg");
    background-position: center;
    background-size: cover;
    height: 100vh;
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
      color: $white;
      position: relative; /* Set position to relative to allow cursor positioning */
      display: inline-block; /* To make the cursor pseudo-element inline */
      text-shadow: 1px 1px 2px black;
      &::after {
        content: "▌"; /* Cursor content */
        position: absolute;
        bottom: 0;
        left: 100%; /* Position cursor after the "User" text */
        animation: blink 1s infinite; /* CSS animation for blinking effect */
        color: $white;
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
    margin-bottom: 2rem;
    width: 65rem;
    height: auto;
    padding-bottom: 2rem;
    border-radius: 10px;
    // box-shadow: 0px 0px 50px $foreground-color;
    box-shadow:
      rgba(0, 0, 0, 0.25) 0px 14px 28px,
      rgba(0, 0, 0, 0.22) 0px 10px 10px;
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
  @media only screen and (max-width: 1076px) {
    .terminal {
      width: 50rem;
    }
  }
  @media only screen and (max-width: 850px) {
    .terminal {
      width: 40rem;
    }
  }
  @media only screen and (max-width: 680px) {
    .terminal {
      width: 30rem;
      height: auto;
      padding-bottom: 2rem;
      margin-bottom: 2rem;
    }
  }
  @media only screen and (max-width: 525px) {
    .terminal {
      width: 25rem;
      margin-bottom: 1rem;
    }
    .flexbox {
      h1 {
        margin-top: 1.6rem;
      }
    }
  }
  @media only screen and (max-width: 440px) {
    .terminal {
      width: 22rem;
    }
  }
  @media only screen and (max-width: 380px) {
    .terminal {
      width: 20rem;
    }
  }
@media only screen and (max-height: 875px) {
  body{
    height: auto;
  }
}
</style>
