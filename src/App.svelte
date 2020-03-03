

<style>
    .container {
        max-width: 900px;
        margin: 0 auto;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 32px;
        font-family: 'Raleway', Roboto, sans-serif;
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
    img{
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
     a:hover{
         color: #333;
     }
    a:focus{
        color: #333;
    }


    @media (max-width: 800px) {
        container{
            font-size: 14px;
            padding: 16px
        }
        .avatar {
            width: 100px;
            height: 100px;
        }
    }
    .box {
        align-items: center;
        flex-direction: column;

    }

</style>

<script>
    let avatar = './static/avatar.jpg';
</script>


  <div class="container">
        <visually-hidden  className='visually-hidden'>Xenia Zhukova's website</visually-hidden>

        <img class="avatar" src={avatar} width="120" height="120" alt="Xenia Zhukova's photo"/>

      <div class="box">
        <h1>Xenia Zhukova</h1>
        <h2>Front-end developer</h2>
      </div>
      <section>
        <h3>Skills</h3>
        <ul>
          <li>Responsive HTML/CSS</li>
          <li>SASS</li>
          <li>Javascript</li>
          <li>React/Redux</li>
          <li>Firebase</li>
          <li>Styled components</li>
        </ul>
      </section>
      <section>
        <h3>Social</h3>
        <ul>
          <li><a href="https://github.com/kporcelainluv">Github</a></li>
          <li><a href="https://t.me/ksushaz">Telegram</a></li>
          <li><a href="mailto:zhukovaksusha@gmail.com">zhukovaksusha@gmail.com</a></li>
        </ul>
      </section>
      <section>
        <h3>Projects</h3>
        <ul>
          <li><a href="https://github.com/kporcelainluv/226838-device">HTML Academy, HTML/CSS 1</a ></li>
          <li><a href="https://github.com/kporcelainluv/226838-sedona-17">HTML Academy, HTML/CSS 2</a ></li>
          <li><a href="https://github.com/kporcelainluv/226838-cinemaddict-10">HTML Academy, JS 2</a ></li>
          <li><a href="https://github.com/kporcelainluv/cinemaddict-react-app">Cinemaddict project in React.js</a ></li>
          <li><a href="https://github.com/kporcelainluv/questionaryProject">Questionary project in React.js</a ></li>
        </ul>
      </section>
      <section>
        <h3>Certificates</h3>
        <ul>
          <li><a href={`static/html1.pdf`}>HTML Academy, HTML/CSS 1</a></li>
          <li><a href={`static/html2.pdf`}>HTML Academy, HTML/CSS 2</a></li>
          <li><a href={`static/JS2.pdf`}>HTML Academy, Java Script 2</a></li>
          <li><a href='https://www.freecodecamp.org/certification/kporcelainluv/javascript-algorithms-and-data-structures'>FreeCodeCamp, JavaScript Algorithms and Data Structures</a></li>
          <li><a href={`#`}>Frontend masters, Complete Intro to React</a></li>
          <li><a href={`#`}>Udemy, Modern React with Redux</a></li>
          <li><a href={`static/Coursera1.pdf`}>Coursera, Introduction to Python</a></li>
          <li><a href={`static/Coursera2.pdf`}>Coursera, Diving into Python</a></li>
          <li><a href={`static/stepik.pdf`}>Stepik.org, Programming on Python</a></li>
          <li><a href={`static/loftschool.pdf`}>Loftschool, Web-development for beginners</a></li>
        </ul>
      </section>
  </div>

