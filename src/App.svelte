<script>
  let avatar = "./static/avatar.jpg";
  let html1 = "./static/html1.pdf";
  let html2 = "./static/html2.pdf";
  let js2 = "./static/JS2.pdf";
  let coursera1 = "./static/Coursera1.pdf";
  let coursera2 = "./static/Coursera2.pdf";
  let stepic = "./static/stepik.pdf";
  let loftschool = "./static/loftschool.pdf";
  let freecodecamp = "https://www.freecodecamp.org/certification/kporcelainluv/javascript-algorithms-and-data-structures"
</script>

<style>
  .container {
    max-width: 900px;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 32px;
    font-family: "Raleway", Roboto, sans-serif;
    font-size: 18px;
    line-height: 32px;
    flex-direction: column;
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
  img {
    justify-content: center;
  }
  h1 {
    margin-bottom: 8px;
  }
  h2 {
    margin: 0 0 8px;
  }
  h3 {
    font-weight: bold;
  }
  a {
    color: black;
  }
  a:hover {
    color: #333;
  }
  a:focus {
    color: #333;
  }
  block {
    align-items: center;
    flex-direction: column;
  }
  @media (max-width: 800px) {
    container {
      font-size: 14px;
      padding: 16px;
    }
    .avatar {
      width: 100px;
      height: 100px;
    }
  }
</style>

<div class="container">
  <visually-hidden className="visually-hidden">
    Xenia Zhukova's website
  </visually-hidden>

  <img
    class="avatar"
    src={avatar}
    width="120"
    height="120"
    alt="Xenia Zhukova's photo" />

  <block>
    <h1>Xenia Zhukova</h1>
    <h2>Front-end developer</h2>
  </block>
  <block>
    <h3>Skills</h3>
    <ul>
      <li>Responsive HTML/CSS</li>
      <li>SASS</li>
      <li>Javascript</li>
      <li>React/Redux</li>
      <li>Firebase</li>
      <li>Styled components</li>
    </ul>
  </block>
  <block>
    <h3>Social</h3>
    <ul>
      <li>
        <a href="https://github.com/kporcelainluv">Github</a>
      </li>
      <li>
        <a href="https://t.me/ksushaz">Telegram</a>
      </li>
      <li>
        <a href="mailto:zhukovaksusha@gmail.com">zhukovaksusha@gmail.com</a>
      </li>
    </ul>
  </block>
  <block>
    <h3>Projects</h3>
    <ul>
      <li>
        <a href="https://github.com/kporcelainluv/226838-device">
          HTML Academy, HTML/CSS 1
        </a>
      </li>
      <li>
        <a href="https://github.com/kporcelainluv/226838-sedona-17">
          HTML Academy, HTML/CSS 2
        </a>
      </li>
      <li>
        <a href="https://github.com/kporcelainluv/226838-cinemaddict-10">
          HTML Academy, JS 2
        </a>
      </li>
      <li>
        <a href="https://github.com/kporcelainluv/cinemaddict-react-app">
          Cinemaddict project in React.js
        </a>
      </li>
      <li>
        <a href="https://github.com/kporcelainluv/questionaryProject">
          Questionary project in React.js
        </a>
      </li>
    </ul>
  </block>
  <block>
    <h3>Certificates</h3>
    <ul>
      <li>
        <a {html1}>HTML Academy, HTML/CSS 1</a>
      </li>
      <li>
        <a {html2}>HTML Academy, HTML/CSS 2</a>
      </li>
      <li>
        <a {js2}>HTML Academy, Java Script 2</a>
      </li>
      <li>
        <a {freecodecamp}>
          FreeCodeCamp, JavaScript Algorithms and Data Structures
        </a>
      </li>
      <li>
        <a {`#`}>Frontend masters, Complete Intro to React</a>
      </li>
      <li>
        <a {`#`}>Udemy, Modern React with Redux</a>
      </li>
      <li>
        <a {coursera1}>Coursera, Introduction to Python</a>
      </li>
      <li>
        <a {coursera2}>Coursera, Diving into Python</a>
      </li>
      <li>
        <a {stepic}>Stepik.org, Programming on Python</a>
      </li>
      <li>
        <a {loftschool}>Loftschool, Web-development for beginners</a>
      </li>
    </ul>
  </block>
</div>
