<script>
  import List from "./List.svelte";
  import Projects from "./Projects.svelte";
  import Certificates from "./Certificates.svelte";
  import Hand from "./Hand.svelte";
  import WorkExperience from "./WorkExperience.svelte";

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
  const bbeCertificate = './static/bbe.png';
  const skills = [
    'Javascript',
    "React",
    'TypeScript',
    'Storybook',
    'Jest',
    "HTML/CSS",


    "Firebase",
    "Styled components",

    'Git',
    'Figma',
    'Miro'
  ];

  const social = [
    { name: "Github", link: "https://github.com/kporcelainluv" },
    { name: "Behance", link: "https://t.me/ksushaz" },
    { name: "Telegram", link: "https://www.behance.net/kseniaz1" },
    { name: "zhukovaksusha@gmail.com", link: "mailto:zhukovaksusha@gmail.com" }]

  const jobs = [
    {name: "Mediafellows", from: 'April 2022', to: 'Present', position: 'Front-end developer',
      description: ['- Developed and tested software applications; ',
      '- Worked closely with the Design team, discussed possible corner cases and improvements;',
        '- Introduced and developed Storybook to organize the UI system;',
        '- Worked as a part of a 7-person team;'],
      tags: ['React', 'TypeScript', 'Mobx', 'Jest', 'CSS Modules', 'Storybook']
    },
    {name: "SGSDT", from: 'May 2020', to: 'September 2021', position: 'Front-end developer', 
      description: ['- Developed functional components and refactored legacy code;',
      '- Developed UI / UX design for several pages, which simplified UX according to hallway testing;',
      '- Teamed up with clients to understand the need for new features and functionality improvement;',
      '- Worked as a part of a 3-person team; '],
      tags: ['React', 'TypeScript', 'Formik', 'Redux', 'SASS', 'Antd']
    },
  ];

  const courses = {
   'UX/UI Design': [{
     name: "UX/UI: Digital product design",
     link: bbeCertificate,
     year: "2021",
     company: "BangBang Education (BBE)"
   }],
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
      }, {
        name: "Asynchronous programming in JS",
        link: '',
        year: "2022",
        company: "Hexlet"
      } ,{
        name: "Introduction to OOP in JS",
        link: '',
        year: "2022",
        company: "Hexlet"
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
        name: "EpicReact",
        link: "",
        year: "2022 - present",
        company: "Kent C.Dodds course at epicreact.dev"
      },
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
      name: "Device - 2019",
      link: "https://226838-device.now.sh/",
      github: "https://github.com/kporcelainluv/226838-device",
      desc:
        "Gadget online store Device. Final project at HTML Academy, HTML/CSS 1",
      tags: ["HTML", "CSS", "Pixel-perfect"]
    },
    {
      name: "Sedona - 2019",
      link: "https://kporcelainluv.github.io/226838-sedona-17/build/",
      github: "https://github.com/kporcelainluv/226838-sedona-17",
      desc:
        "Arizona Tourist Campus Site. Final project at HTML Academy, HTML/CSS 2",
      tags: ["HTML", "BEM", "SASS", "Gulp", "Adaptive CSS"]
    },
    {
      name: "Cinemaddict - 2019",
      link: "https://226838-cinemaddict-10.now.sh/",
      github: "https://github.com/kporcelainluv/226838-cinemaddict-10",
      desc:
        "Service for fans of movies. Final project at HTML Academy, Javascript 2",
      tags: ["JS", "ES2016", "Webpack", "OOP", "Rest", "Service Worker"]
    },
    {
      name: "Cinemaddict in React.js - 2020",
      link: "https://cinemaddict-react-app.now.sh/",
      github: "https://github.com/kporcelainluv/cinemaddict-react-app",
      desc: "Service for fans of movies rewritten in React.js."
    },
    {
      name: "Questionary - 2020",
      link: "https://zhukovairina.now.sh/",
      github: "https://github.com/kporcelainluv/questionaryProject",
      desc: `An app that I've built for my mom in React.js.
        She has a need to collect data from clients before the lessons she holds.`,
      screenshots: true,
      tags: ["React", "Firebase", "Telegram API"]
    },
    {
      name: "React exercises - 2020",
      link: "https://react-practice.now.sh/",
      github: "https://github.com/kporcelainluv/react-practice",
      desc: "In that project I solved simple tasks while learning React."
    },
    {
      name: "Doctors' Alliance - 2020",
      link: "https://fbk-test.zhukovaxenia.now.sh/",
      github: "https://github.com/kporcelainluv/fbk-test",
      desc: "A test project done for FBK in React.js",
      tags: ["React", "styled-components", "Adaptive CSS"]
    },
    {
      name: "Smart Home App UI/UX Prototype - 2021",
      link: "https://www.behance.net/gallery/143961221/Smart-home-app",
      github: null,
      desc: "The app helps tenants to interact with the developer,  management organization, neighbors, " +
              "and the entire infrastructure of a smart apartment complex.",
      tags: ["UX/UI",  'UX Research', "Figma", "Miro", ]
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
    width: 375px;
  }
  h1 {
    margin-bottom: 8px;
  }
  h2 {
    margin: 0 0 8px;
    font-size: 1.2em;
    line-height: 1.2em;
    font-weight: 400;
  }
  h2 span {
    display: block;
  }
  h3 {
    font-size: 1em;
    font-weight: bold;
    margin: 32px 0 0;
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
      <Hand />
    </div>

    <div class="centered">
      <h1>Xenia Zhukova</h1>
      <h2>
        <span>Front-end dev & Product Designer</span>
        <span> 2+ years of experience</span>
        </h2>
    </div>
    <block>
      <h3>Social</h3>
      <List elements={social} />
    </block>
    <block>
      <h3>Employment history</h3>
      <WorkExperience {jobs} />
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
