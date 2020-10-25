<!--
# portfolio
personal portfolio

-->


<!--

FCC test tracker

<script src="https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js"></script>
-->


<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <meta name="website" content="fcc portfolio">
    <title>Personal Portfolio Webpage</title>

    <style>

    :root {
    --white: #f0f0f0;
    --red: #be3144;
    --blue: #25567d;
    --gray: #303841;
    }

    * {
      margin: 0;
      padding: 0;
    }

    *,
    *::before,
    *::after {
      box-sizing: inherit;
    }

    html {
      box-sizing: border-box;
      font-size: 62.5%;
      scroll-behaviour: smooth;
    }

    @media (max-width: 75em) {
      html {
        font-size: 60%;
      }
    }

    @media (max-width: 61.25em) {
      html {
        font-size: 58%;
      }
    }

    @media (max-width: 28.75em) {
      html {
      font-size: 55%;
      }
    }

    body {
      font-family: 'Poppins', sans-serif;
      font-size: 1.8em;
      font-weight: 400;
      line-height: 1.4;
      color: ;

    }

    h1,
    h2 {
      font-family: 'Raleway', sans-serif;
      font-weight: 700;
      text-align: center;
    }

    h1 {
      font-size: 5em;
    }

    h2 {
      font-size: 4.2em;
    }

    ul {
      list-style: none;
    }

    a {
      text-decoration: none;
      color: #f0f0f0;
    }

    img {
      display: block;
      width: 100%;
    }

    .bon-iver {
        filter: gray;
      -webkit-filter: grayscale(1);
      filter: grayscale(1);
      height: 325px; width: 162.5px;
    }

    .nav {
      display: flex;
      justify-content: flex-end;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: #be3144;
      box-shadow: 0 2px 0 rgba(0, 0, 0, 0.4);
      z-index: 10;
    }

    .nav-list {
      display: flex;
      margin-right: 2rem;
    }

    @media (max-width: 28.75) {
      .nav {
        justify-content: center;
      }

      .nav-list {
        margin: 0 1rem;
      }
    }

    .nav-list a {
      display: block;
      font-size: 2.2rem;
      padding: 2rem;
    }

    .nav-list a:hover {
      background: #25567d;
    }

    .welcome-section {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: 100vh;
      background-color: #000;
      background-image: linear-gradient(62deg, #3a3d40 0%, #181719 100%);
    }

    .welcome-section > h1 {
      color: #f0f0f0;
    }
    .welcome-section > p {
      font-size: 3rem;
      font-weight: 200;
      font-style: italic;
      color: #be3144;
    }

    .projects-section {
      text-align: center;
      padding: 10rem 2rem;
      background: #25567d;
    }

    .projects-section-header {
      max-width: 640px;
      margin: 0 auto 6rem auto;
      border-bottom: 0.2rem solid #f0f0f0;
    }

    @media (max-width: 28.75em) {
      .projects-section-header {
        font-size: 4rem;
      }  
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      grid-gap: 4rem;
      width: 100%;
      max-width: 1280px;
      margin: 0 auto;
      margin-bottom: 6rem;
    }

    @media (max-width: 30.625em) {
      .projects-section {
        padding: 6rem 1rem;
      }
    }

    .projects-grid {
      grid-template-columns: 1fr;
    }

    .project {
      background: #303841;
      box-shadow: 1px 10px 20px rgba(0, 0, 0, 0.4);
      border-radius: 2px;
    }

    .code {
      color: #303841;
      transition: color 0.3s ease-out;
    }

    .project:hover .code {
      color: #ff7f50;
    }

    .project-image {
      height: calc(100% - 6.8rem);
      width: 100%;
      object-fit: cover;
    }

    .project-title {
      font-size: 2rem;
      padding: 2rem 0.5rem;
    }

    .btn {
      display: inline-block;
      padding: 1rem 2rem;
      border-radius: 2px;
    }

    .btn-show-all {
      font-size: 2rem;
      background: #303841;
      transition: background 0.3s ease-out;
    }

    .btn-show-all:hover {
      background: #be3144;
    }


    .contacts-section {
      display:flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      width: 100%;
      height: 80vh;
      padding: 0 2rem;
      background: #303841;

    }

    .contacts-section-header > h2 {
      font-size: 6rem;
      color: #f0f0f0;

     }

    @media (max-width: 28.75em) {
      .contacts-section-header > h2 {
      font-size: 4rem;
      text-align: center;
      }
    }

    .contacts-section-header > p {
      font-style: italic;
      text-align: center;
      color: #f0f0f0;
    }

    .contact-links {
      display: flex;
      justify-content: center;
      width: 100%;
      max-width: 980px;
      margin-top: 4rem;
      flex-wrap: wrap;
    }

    .contact-details {
      font-size: 2.4rem;
      text-shadow: 2px 2px 1px #1f1f1f;
      transition: transform 0.3s ease-out;
    }

    .contact-details:hover {
      transform: translateY(8px);
    }

    footer {
      font-weight: 300;
      display: flex;
      justify-content: space-evenly;
      padding: 2rem;
      background: #303841;
      border-top: 4px solid #be3144;
    }
    footer > p {
      margin: 2rem;
    }

    @media (max-width: 28.75) {
      footer {
        flex-direction: column;
        text-align: center;
      }
    }

    </style>

  </head>  
  <body>
    <nav id="navbar" class="nav">
      <ul class="nav-list">
        <li>
        <a href="#welcome-section">About</a>
        </li>
        <li>
          <a href="#projects">Work</a>
        </li>
        <li>
          <a href="#contact">Contact</a>
        </li>
      </ul>
    </nav>  

    <section id="welcome-section" class="welcome-section">
      <h1>Hugh Burgess - Portfolio</h1>
      <p>Learning step-by-step to code.</p>
    </section>  

    <section id="projects" class="projects-section">
      <h2 class="projects-section-header">An overview of my projects</h2>
      <div class="projects-grid">
        <a href="https://codepen.io/hugh-burgess/full/gOMpMbR" target="_blank" class="project project-title project-tile">
          <img class="project-image bon-iver" src="https://media.pitchfork.com/photos/592c6dd7c0084474cd0c7d6b/2:1/w_648/86f9142c.jpg" alt="project">
          <p class="project-title">
            <span class="code"><</span>
              Tribute Page
              <span class="code">/></span>
          </p>
        </a>

        <a href="https://codepen.io/hugh-burgess/full/ZEOGKGa" target="_blank" class="project project-title project-tile">
          <img class="project-image" src="https://cdn.freecodecamp.org/testable-projects-fcc/images/survey-form-background.jpeg" alt="project">
          <p class="project-title">
            <span class="code"><</span>
              Survey Page
              <span class="code">/></span>
          </p>
        </a>

        <a href="https://codepen.io/hugh-burgess/full/vYKGzLX" target="_blank" class="project project-title project-tile">
          <img class="project-image" src="https://images.unsplash.com/photo-1558544956-15f3c317e06a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80" alt="project">
          <p class="project-title">
            <span class="code"><</span>
              Product Landing Page
              <span class="code">/></span>
          </p>
        </a>


        <a href="https://codepen.io/hugh-burgess/full/MWeebWg" target="_blank" class="project project-title project-tile">
          <img class="project-image" src="https://images.unsplash.com/photo-1512295767273-ac109ac3acfa?ixlib=rb-1.2.1&auto=format&fit=crop&w=675&q=80" alt="project">
          <p class="project-title">
            <span class="code"><</span>
              Technical Documentation Page
              <span class="code">/></span>
          </p>
        </a>      



      </div>
      <a class="btn btn-show-all" href="https://codepen.io/your-work/" target="_blank">Show all</a>
    </section>  

    <section id="contact" class="contacts-section">
      <div class="contacts-section-header">
        <h2>Get in touch...</h2>
        <p>Let's connect!</p>
      </div>

      <div class="contact-links">
        <a class="btn contact-details" href="https://twitter.com/hughburgess" id="profile-link" target="_blank">Twitter</a>
        <a href="mailto:hughburgessgermany@hotmail.com" class="btn contact-details">Mail Me</a>
        <a id="profile-link" href="https://github.com/hugh-burgess" target="_blank" class="btn contact-details">GitHub</a>
        <a href="https://hughburgess.medium.com" target="_blank" class="btn contact-details">Medium</a>
        <a href="https://www.linkedin.com/in/hugh-burgess-1750b485/" target="_blank" class="btn contact-details">LinkedIn</a>      
      </div>
    </section>

    <footer>
      <p>&copy; Created by Hugh Burgess 2020</p>
    </footer>



  </body>
</html>
