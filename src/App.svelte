<script>
  import List from "./List.svelte";
  import Projects from "./Projects.svelte";
  import Certificates from "./Certificates.svelte";
  import Hand from "./Hand.svelte";

  const avatar = "./static/avatar.jpg";
  const html1 = "./static/html1.pdf";
  const html2 = "./static/html2.pdf";
  const js2 = "./static/JS2.pdf";
  const coursera1 = "./static/Coursera1.pdf";
  const coursera2 = "./static/Coursera2.pdf";
  const stepic = "./static/stepik.pdf";
  const loftschool = "./static/loftschool.pdf";
  const freecodecamp =
    "https://www.freecodecamp.org/certification/kporcelainluv/javascript-algorithms-and-data-structures";
  const algorithmicToolbox = "./static/algorithmic_toolbox1.pdf";
  const jquery = "./static/jquery.png";
  const udacityHtml = "./static/udacityHtml.png";
  const udacityPython = "./static/UdacityPython.png";
  const devman = "./static/devman.png";
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

  const courses = {
    Algorithms: [
      {
        name: "JS Algorithms and Data Structures",
        link: freecodecamp,
        year: "2019",
        company: "FreeCodeCamp"
      },
      {
        name: "Algorithmic Toolbox part 1",
        link: algorithmicToolbox,
        year: "2019",
        company: "Coursera"
      }
    ],
    Javascript: [
      {
        name: "JavaScript level 2",
        link: js2,
        year: "2020",
        company: "HTML Academy"
      },
      {
        name: "Intro to jQuery",
        link: jquery,
        year: "2017",
        company: "Udacity"
      }
    ],
    "HTML&CSS": [
      {
        name: "HTML/CSS level 2",
        link: html2,
        year: "2019",
        company: "HTML Academy"
      },
      {
        name: "HTML/CSS level 1",
        link: html1,
        year: "2019",
        company: "HTML Academy"
      },

      {
        name: "Intro to HTML&CSS",
        link: udacityHtml,
        year: "2017",
        company: "Udacity"
      },
      {
        name: "Web-development for beginners",
        link: loftschool,
        year: "2016",
        company: "Loftschool"
      }
    ],

    React: [
      {
        name: "Modern React with Redux",
        link: "",
        year: "2020",
        company: "Udemy"
      },
      {
        name: "Complete Intro to React",
        link: "",
        year: "2019",
        company: "Frontend masters"
      }
    ],

    Python: [
      {
        name: "Diving into Python",
        link: coursera2,
        year: "2018",
        company: "Coursera"
      },
      {
        name: "Programming on Python",
        link: stepic,
        year: "2018",
        company: "Stepik.org"
      },
      {
        name: "Introduction to Python",
        link: coursera1,
        year: "2018",
        company: "Coursera"
      },
      {
        name: "Devman problems",
        link: devman,
        year: "2017",
        company: "Devman"
      },
      {
        name: "Programming foundations with Python",
        link: udacityPython,
        year: "2017",
        company: "Udacity"
      }
    ]
  };

  const projects = [
    {
      name: "Device",
      link: "https://226838-device.now.sh/",
      github: "https://github.com/kporcelainluv/226838-device",
      desc:
        "Gadget online store Device. Final project at HTML Academy, HTML/CSS 1",
      tags: ["HTML", "CSS", "Pixel-perfect"]
    },
    {
      name: "Sedona",
      link: "https://kporcelainluv.github.io/226838-sedona-17/build/",
      github: "https://github.com/kporcelainluv/226838-sedona-17",
      desc:
        "Arizona Tourist Campus Site. Final project at HTML Academy, HTML/CSS 2",
      tags: ["HTML", "BEM", "SASS", "Gulp", "Adaptive CSS"]
    },
    {
      name: "Cinemaddict",
      link: "https://226838-cinemaddict-10.now.sh/",
      github: "https://github.com/kporcelainluv/226838-cinemaddict-10",
      desc:
        "Service for fans of movies. Final project at HTML Academy, Javascript 2",
      tags: ["JS", "ES2016", "Webpack", "OOP", "Rest", "Service Worker"]
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
        She has a need to collect data from clients before the lessons she holds.`,
      screenshots: true,
      tags: ["React", "Firebase", "Telegram API"]
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
  :global(html) {
    background-color: rgba(242, 242, 230, 0.1);
    color: #242535;
    font-family: "Helvetica Neue", sans-serif;
  }
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
    font-size: 22px;
    font-weight: bold;
    margin: 28px 0 14px;
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
      <Hand />
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
      <Certificates {courses} />
    </block>
  </div>
</container>
