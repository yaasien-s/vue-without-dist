<template>
<section id="project-card">
<div class="project-card">   
  <div v-if="getProject" class="project-details">
    <h1>{{ getProject.title }}</h1>
    <img :src="getProject.image" alt="" id="one">
    <!-- <p>ID: {{ project.id }}</p> -->
    <h5 class="my-4">{{ getProject.details }}</h5>
    <a :href="getProject.github" target="_blank"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-github" viewBox="0 0 16 16">
  <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
</svg> Github</a> <a :href="getProject.link" target="_blank"><svg width="24" height="24" viewBox="0 0 256 256" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" preserveAspectRatio="xMidYMid" fill="currentColor">
    <g>
        <path d="M153.094392,165.678589 L90.3094111,152.558384 C90.0414069,153.070392 89.7534024,153.566399 89.4333974,154.034407 L146.59029,237.41171 L150.038344,233.967656 L159.762496,173.498711 C156.454445,172.110689 153.966406,169.210644 153.094392,165.678589 L153.094392,165.678589 Z M130.190034,83.6053063 C127.837997,87.2133627 123.777934,89.6014 119.153862,89.6014 C118.441851,89.6014 117.74984,89.5293989 117.069829,89.4213972 L88.4373818,134.222097 L164.934577,101.301583 C164.910577,100.993578 164.842576,100.705574 164.842576,100.389569 C164.842576,99.7455585 164.930577,99.1215488 165.034579,98.5055391 L130.190034,83.6053063 L130.190034,83.6053063 Z M132.270067,75.4411788 L169.334646,91.2894264 C170.506664,90.3734121 171.842685,89.6934015 173.310708,89.281395 L179.402803,51.4008031 L156.194441,28.1924405 L130.070032,69.0690792 C131.322052,70.9171081 132.098064,73.0931421 132.270067,75.4411788 L132.270067,75.4411788 Z M209.93528,81.9332802 L186.674917,58.6689167 L181.618838,90.0774075 C182.906858,90.7294176 184.054876,91.5974312 185.014891,92.6614478 L209.93528,81.9332802 L209.93528,81.9332802 Z M154.206409,157.406459 C156.018438,154.130408 159.36249,151.866373 163.294551,151.562368 L169.974656,110.013719 C169.450648,109.665714 168.98264,109.249707 168.522633,108.8217 L91.585431,141.934218 C91.7814341,142.73823 91.9174362,143.558243 91.9814372,144.410256 L154.206409,157.406459 L154.206409,157.406459 Z M216.271379,88.2733793 L189.358959,99.8535602 L255.759996,128.242004 L256,128.002 L216.271379,88.2733793 L216.271379,88.2733793 Z M168.178628,173.622713 L160.090501,223.907499 L207.055235,176.942765 L173.226707,169.878654 C171.934686,171.562681 170.202659,172.866701 168.178628,173.622713 L168.178628,173.622713 Z M76.8932015,160.694511 C75.1931749,160.694511 73.5651495,160.402506 72.0411256,159.886498 L56.4408819,184.29888 L50.4127877,178.274786 L65.1890186,155.154424 C64.8210128,154.702417 64.4850076,154.22641 64.1690026,153.738402 L37.4005844,165.262582 L31.0564853,158.918483 L60.3569431,146.306286 L7.38411538,135.250113 L0.140002188,128.002 L2.432038,125.709964 L63.5169925,138.462163 C64.2250035,137.126143 65.1250176,135.898123 66.1850341,134.846107 L36.5365709,91.6014313 L42.5246644,85.6133377 L73.5011485,130.798044 C74.5931655,130.55004 75.7251832,130.402038 76.8932015,130.402038 C78.2012219,130.402038 79.4692417,130.58604 80.6812606,130.898045 L109.665714,85.5453366 C107.393678,83.1772996 105.989656,79.9692495 105.989656,76.4291942 C105.989656,75.389178 106.121658,74.3811622 106.349662,73.4131471 L70.1890967,57.9529055 L76.5331958,51.6088064 L110.793731,66.2610353 C113.069767,64.3890061 115.981812,63.2649885 119.157862,63.2649885 C120.657885,63.2649885 122.097908,63.5289926 123.445929,63.9929999 L150.170346,22.1683464 L128.002,0 L0,128.002 L128.002,256.004 L140.598197,243.407803 L83.0132971,159.398491 C81.1372678,160.226504 79.0692355,160.694511 76.8932015,160.694511 L76.8932015,160.694511 Z M178.122783,111.805747 L171.326677,154.042407 C173.666714,155.930436 175.226738,158.69448 175.522743,161.854529 L214.095345,169.906655 L249.415897,134.586103 L185.662901,107.329677 C183.874873,109.705714 181.202831,111.35374 178.122783,111.805747 L178.122783,111.805747 Z"></path>
    </g>
</svg> Live</a>
<br>
      <button @click="back" id="Back">Go Back</button>

  </div>
  <div v-else id="preload">
      Loading project data...
  </div>
</div>

</section>
</template>

<script>
export default {
    props: ['id'],
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
            "title": "J.S Calcultor",
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
          }

        ],
            project: null
        }
    },
    // mounted() {
    //     fetch('http://localhost:3000/project/' + this.$route.params.id)
    //     .then(res => res.json())
    //     .then(data => {
    //         console.log(data);
    //         this.project = data
    //     })
    //     .catch(err => console.log(err.message))
    // },
    methods: {
         back() {
      this.$router.go(-1)
    },
    },
    computed: {
        getProject(){
            return this.projects.find(project => project.id == this.$route.params.id)
        }
    }
}
</script>

<style>
#project-card {
    margin-top: 100px;
}
.project-card {
    width: 90%;
    display: flex;
    flex-direction: column;
    color: #000;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 25);
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 100px;
}
.project-details {
     background: #2b2b26;
    padding: 20px;
    border-radius: 10px;
    margin: 10px auto;
    max-width: 600px;
    cursor: pointer;
    color: #568259;
    margin-top: 100px;
    margin-bottom: 50px;
}

.project-details h1 {
    color: #568259;
}

.project-details img {
    border-radius: 10px;
}

.project-details p {
    font-weight: 600;
}

.project-details a {
    color: #568259;
    text-decoration: none;
    font-weight: 600;
    font-size: 18px;
    background: #2b2b26;
    /* border: #568259 1px solid; */
    border-radius: 5px;
    transition: 00.3s;
    padding: 5px;
    box-shadow: rgba(48, 48, 48, 0.25) 0px 30px 60px -12px inset, rgba(0, 0, 0, 0.3) 0px 18px 36px -18px inset;
}
.project-details a:hover {
    color: #2b2b26;
    text-decoration: underline;
    transition: 00.3s;
    background: #568259;
    border: none;
    transition: 0.3s;
    box-shadow: rgba(0, 0, 0, 0.17) 0px -23px 25px 0px inset, rgba(0, 0, 0, 0.15) 0px -36px 30px 0px inset, rgba(0, 0, 0, 0.1) 0px -79px 40px 0px inset, rgba(0, 0, 0, 0.06) 0px 2px 1px, rgba(0, 0, 0, 0.09) 0px 4px 2px, rgba(0, 0, 0, 0.09) 0px 8px 4px, rgba(0, 0, 0, 0.09) 0px 16px 8px, rgba(0, 0, 0, 0.09) 0px 32px 16px;
}
#Back {
  margin-top: 30px;
  padding: 10px;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  background: #568259;
  color: #2b2b26;
  box-shadow: rgba(0, 0, 0, 0.17) 0px -23px 25px 0px inset, rgba(0, 0, 0, 0.15) 0px -36px 30px 0px inset, rgba(0, 0, 0, 0.1) 0px -79px 40px 0px inset, rgba(0, 0, 0, 0.06) 0px 2px 1px, rgba(0, 0, 0, 0.09) 0px 4px 2px, rgba(0, 0, 0, 0.09) 0px 8px 4px, rgba(0, 0, 0, 0.09) 0px 16px 8px, rgba(0, 0, 0, 0.09) 0px 32px 16px;
  width: fit-content;
  margin-left: auto;
  margin-right: auto;
  transition: 00.3s;
}
#Back:hover {
    background: #2b2b26;
    color: #568259;
    /* border: #2b2b26 1px solid; */
    font-weight: 600;
    box-shadow: rgba(0, 0, 0, 0.17) 0px -23px 25px 0px inset, rgba(0, 0, 0, 0.15) 0px -36px 30px 0px inset, rgba(0, 0, 0, 0.1) 0px -79px 40px 0px inset, rgba(0, 0, 0, 0.06) 0px 2px 1px, rgba(0, 0, 0, 0.09) 0px 4px 2px, rgba(0, 0, 0, 0.09) 0px 8px 4px, rgba(0, 0, 0, 0.09) 0px 16px 8px, rgba(0, 0, 0, 0.09) 0px 32px 16px;
    transition: 0.3s;
}
#preload {
    margin-top: 100px;
}
#one {
    width: 75%;
}

@media (max-width: 1100px) {
    .project-details {
        max-width: 85%;
    }
}
</style>