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
      name: "HTML Academy, HTML/CSS 1",
      link: "https://github.com/kporcelainluv/226838-device",
      desc: "Introduction to HTML and CSS project. "
    },
    {
      name: "HTML Academy, HTML/CSS 2",
      link: "https://github.com/kporcelainluv/226838-sedona-17",
      desc: "HTML/SASS project. Uses Gulp and BAM."
    },
    {
      name: "HTML Academy, JS 2",
      link: "https://github.com/kporcelainluv/226838-cinemaddict-10",
      desc:
        "Object-oriented programming project. Moowle website fetches favorite films from server and displays to user. Favorite films, history, statistics pages are available."
    },
    {
      name: "Cinemaddict project in React.js",
      link: "https://github.com/kporcelainluv/cinemaddict-react-app",
      desc: "Project written with React state."
    },
    {
      name: "Questionary project in React.js",
      link: "https://github.com/kporcelainluv/questionaryProject",
      desc:
        "Questionary made for business to gather data. Has a list of users and user profile avaliable for whitelist users. Uses Firebase to save data. Connected to Telegram bot."
    },
    {
      name: "React exercises",
      link: "https://github.com/kporcelainluv/react-practice",
      desc:
        "Simple projects in React.js like To-do list, Counter, Fetch API, Current time"
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
    font-family: "Raleway", Roboto, sans-serif;
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
  h2 {
    margin: 0 0 8px;
  }
  h3 {
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
