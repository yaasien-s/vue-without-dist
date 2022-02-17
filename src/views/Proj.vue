<template>
  <section id="projects">
    <div class="projects">
      <h1 class="a-h1">Project Page</h1>
      <div v-if="projects.length" class="proj">
        <div v-for="project of projects" :key="project.id" class="project">
          <router-link :to="{ name: 'Projects', params: { id: project.id }}">
            <h2>{{ project.title }}</h2>
          </router-link>
        </div>
      </div>
      <div v-else>
        <p id="preload">Loading projects...</p>
      </div>
      <router-link to="/" id="home"><svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#fff"
          class="bi bi-house-fill" viewBox="0 0 16 16">
          <path fill-rule="evenodd"
            d="m8 3.293 6 6V13.5a1.5 1.5 0 0 1-1.5 1.5h-9A1.5 1.5 0 0 1 2 13.5V9.293l6-6zm5-.793V6l-2-2V2.5a.5.5 0 0 1 .5-.5h1a.5.5 0 0 1 .5.5z" />
          <path fill-rule="evenodd"
            d="M7.293 1.5a1 1 0 0 1 1.414 0l6.647 6.646a.5.5 0 0 1-.708.708L8 2.207 1.354 8.854a.5.5 0 1 1-.708-.708L7.293 1.5z" />
        </svg></router-link>
    </div>

    <footer>© 2022 Yaasien Salaam ALL RIGHTS RESERVED</footer>


  </section>
</template>

<script>
  export default {
    data() {
      return {
        projects: [{
            "id": 1,
            "image": "https://i.postimg.cc/LsLhhbyG/Muhammad-Yaasien-Salaam-Google-Chrome-2021-10-27-11-40-22-edited.jpg",
            "title": "First Project",
            "details": "My very first website I built",
            "github": "https://github.com/yaasien-s/my-css-site",
            "link": "https://yaasien-1.netlify.app/"
          },
          {
            "id": 2,
            "image": "https://i.postimg.cc/Sx33gy6Y/Screenshot-10.png",
            "title": "BMI Calculator",
            "details": "Created a BMI calculator using JavaScript",
            "github": "https://github.com/yaasien-s/BMI-Calculator",
            "link": "https://yaasiensbmi.netlify.app/"
          },
          {
            "id": 3,
            "image": "https://i.postimg.cc/zB1M10PJ/Screenshot-11.png",
            "title": "Point of Sales",
            "details": "Created an online shopping store using JavaScript",
            "github": "https://github.com/yaasien-s/Point-of-sale",
            "link": "https://yaasien-pos.netlify.app/"
          },
          {
            "id": 4,
            "image": "https://i.postimg.cc/tg6ffLkS/Screenshot-12.png",
            "title": "J.S Calculator",
            "details": "First Calculator I created",
            "github": "https://github.com/yaasien-s/JavaScript-calculator",
            "link": "https://javascript-calculator-ys.netlify.app/"
          },
          {
            "id": 5,
            "image": "https://i.postimg.cc/bJH5YkK1/Screenshot-13.png",
            "title": "Portfolio",
            "details": "Previous porfolio used.",
            "github": "https://github.com/yaasien-s/Trident",
            "link": "https://yaasiensalaam.netlify.app/"
          },
          {
            "id": 6,
            "image": "https://i.postimg.cc/nLYdzj7H/Muhammad-Yaasien-Salaam-Google-Chrome-2021-10-27-11-43-23-edited.jpg",
            "title": "Peaceful Watches",
            "details": "Mini project made with bootstrap.",
            "github": "https://github.com/yaasien-s/bootstrapweb",
            "link": "https://peaceful-watches.netlify.app/"
          }


        ]
      }
    },

  }
</script>

<style>
  .a-h1 {
    margin-top: 25px;
    margin-bottom: 25px;
  }

  #projects {
    margin-top: 100px;
  }

  .projects {
    width: 90%;
    display: flex;
    flex-direction: column;
    color: #000;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 25);
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 50px;
  }

  .proj {
    /* margin-top: 100px; */
    margin-bottom: 100px;
  }

  .project h2 {
    background: #2b2b26;
    padding: 20px;
    border-radius: 10px;
    margin: 10px auto;
    max-width: 600px;
    cursor: pointer;
    transition: 00.3s;
    color: #568259;
  }

  .project h2:hover {
    transition: 00.3s;

    background: #78b47c;
    color: #2b2b26;
    /* border: #2b2b26 1px solid; */
    transition: 0.3s ease-in-out;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 30px 60px -12px inset, rgba(0, 0, 0, 0.3) 0px 18px 36px -18px inset;
  }

  .project a {
    text-decoration: none;
  }


  @media (max-width: 650px) {
    .project h2 {
      max-width: 75%;
    }
  }
</style>