<script>
  import List from "./List.svelte";
  import Projects from "./Projects.svelte";

  let avatar = "./static/avatar.jpg";
  let html1 = "./static/html1.pdf";
  let html2 = "./static/html2.pdf";
  let js2 = "./static/JS2.pdf";
  let coursera1 = "./static/Coursera1.pdf";
  let coursera2 = "./static/Coursera2.pdf";
  let stepic = "./static/stepik.pdf";
  let loftschool = "./static/loftschool.pdf";
  let freecodecamp =
    "https://www.freecodecamp.org/certification/kporcelainluv/javascript-algorithms-and-data-structures";

  const skills = [
    "Responsive HTML/CSS",
    "SASS",
    "Javascript",
    "React/Redux",
    "Firebase",
    "Styled components"
  ];

  const social = [
    { name: "Github", link: "https://github.com/kporcelainluv" },
    { name: "Telegram", link: "https://t.me/ksushaz" },
    { name: "zhukovaksusha@gmail.com", link: "mailto:zhukovaksusha@gmail.com" }
  ];

  const courses = [
    { name: "HTML Academy, HTML/CSS 1", link: html1 },
    { name: "HTML Academy, HTML/CSS 2", link: html2 },
    { name: "HTML Academy, JavaScript 2", link: js2 },
    {
      name: "FreeCodeCamp, JS Algorithms and Data Structures",
      link: freecodecamp
    },
    { name: "Frontend masters, Complete Intro to React", link: "" },
    { name: "Udemy, Modern React with Redux", link: "" },
    { name: "Coursera, Introduction to Python", link: coursera1 },
    { name: "Coursera, Diving into Python", link: coursera2 },
    { name: "Stepik.org, Programming on Python", link: stepic },
    { name: "Loftschool, Web-development for beginners", link: loftschool }
  ];

  const projects = [
    {
      name: "Device",
      link: "https://226838-device.now.sh/",
      github: "https://github.com/kporcelainluv/226838-device",
      desc:
        "Gadget online store Device. Final project at HTML Academy, HTML/CSS 1"
    },
    {
      name: "Sedona",
      link: "https://kporcelainluv.github.io/226838-sedona-17/build/",
      github: "https://github.com/kporcelainluv/226838-sedona-17",
      desc:
        "Arizona Tourist Campus Site. Final project at HTML Academy, HTML/CSS 2"
    },
    {
      name: "Cinemaddict",
      link: "https://226838-cinemaddict-10.now.sh/",
      github: "https://github.com/kporcelainluv/226838-cinemaddict-10",
      desc:
        "Service for fans of movies.Final project at HTML Academy, Javascript 2"
    },
    {
      name: "Cinemaddict in React.js",
      link: "https://cinemaddict-react-app.now.sh/",
      github: "https://github.com/kporcelainluv/cinemaddict-react-app",
      desc: "Service for fans of movies rewritten in React.js."
    },
    {
      name: "Questionary",
      link: "https://zhukovairina.now.sh/",
      github: "https://github.com/kporcelainluv/questionaryProject",
      desc: `An app that I've built for my mom in React.js.
        She has a need to collect data from clients before the lessons she holds.
        The app has a list of users and user profile available for whitelist users.
        Uses Firebase to save data. Connected to Telegram bot.`,
      screenshots: true
    },
    {
      name: "React exercises",
      link: "https://react-practice.now.sh/",
      github: "https://github.com/kporcelainluv/react-practice",
      desc: "In that project I solved simple tasks while learning React."
    }
  ];
</script>

<style>
  container {
    max-width: 900px;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 32px;
    font-family: "Helvetica Neue", sans-serif;
    font-size: 18px;
    line-height: 32px;
    color: #181919;
  }
  visually-hidden {
    position: absolute;
    width: 1px;
    height: 1px;
    margin: -1px;
    border: 0px;
    padding: 0px;
    clip: rect(0 0 0 0);
    overflow: hidden;
  }
  block {
    align-items: center;
    flex-direction: column;
  }
  .centered {
    text-align: center;
  }
  .main {
    width: 400px;
  }
  h1 {
    margin-bottom: 8px;
  }
  h2 {
    margin: 0 0 8px;
  }
  h3 {
    font-size: 18px;
    font-weight: bold;
    margin-bottom: 0;
  }
  ul {
    margin-top: 8px;
  }
  @media (max-width: 500px) {
    container {
      font-size: 16px;
    }
    .avatar {
      width: 100px;
      height: 100px;
    }
    .main {
      width: 300px;
    }
  }
</style>

<container>
  <div class="main">
    <visually-hidden className="visually-hidden">
      Xenia Zhukova's website
    </visually-hidden>
    <div class="centered">
      <img
        class="avatar"
        src={avatar}
        width="120"
        height="120"
        alt="Xenia Zhukova's photo" />
    </div>

    <div class="centered">
      <h1>Xenia Zhukova</h1>
      <h2>Front-end developer</h2>
    </div>
    <block>
      <h3>Social</h3>
      <List elements={social} />
    </block>
    <block>
      <h3>Skills</h3>
      <ul>
        {#each skills as skill}
          <li>{skill}</li>
        {/each}
      </ul>
    </block>
    <block>
      <h3>Projects</h3>
      <Projects {projects} />
    </block>
    <block>
      <h3>Certificates</h3>
      <List elements={courses} />
    </block>
  </div>
</container>
