<template>
<section id="resume">
	<div class="resume">
		 <div class="resumes-heading">
      <h1 id="R-h1">Resume</h1>
    </div>
    <div class="resumes-container">
      <div class="resume" v-for="resume of resumes" :key="resume">
        <div class="resume-content">
			<div class="row">
				<div class="col-sm-2">
			<img :src="resume.image" alt="">
			</div>
			<div class="col-sm-10">
          <h2>{{ resume.name }}</h2>
		  </div>
		  </div>
          <p>{{ resume.content }}</p>
          <cite>{{ resume.title }}</cite>
        </div>
      </div>
    </div>

	<h1>Technical Skills</h1>
	<div class="row text-align-center mx-0">
	<div class="col-sm-3"><svg aria-hidden="true" focusable="false" height="64" width="64" data-prefix="fab" data-icon="html5" class="skill-icon mx-5 my-5 svg-inline--fa fa-html5 fa-w-12" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512"><path fill="#E44D26" d="M0 32l34.9 395.8L191.5 480l157.6-52.2L384 32H0zm308.2 127.9H124.4l4.1 49.4h175.6l-13.6 148.4-97.9 27v.3h-1.1l-98.7-27.3-6-75.8h47.7L138 320l53.5 14.5 53.7-14.5 6-62.2H84.3L71.5 112.2h241.1l-4.4 47.7z"></path></svg></div>
	<div class="col-sm-3"><svg aria-hidden="true" focusable="false" height="64" width="64" data-prefix="fab" data-icon="css3-alt" class="skill-icon mx-5 my-5 svg-inline--fa fa-css3-alt fa-w-12" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512"><path fill="#347DC6" d="M0 32l34.9 395.8L192 480l157.1-52.2L384 32H0zm313.1 80l-4.8 47.3L193 208.6l-.3.1h111.5l-12.8 146.6-98.2 28.7-98.8-29.2-6.4-73.9h48.9l3.2 38.3 52.6 13.3 54.7-15.4 3.7-61.6-166.3-.5v-.1l-.2.1-3.6-46.3L193.1 162l6.5-2.7H76.7L70.9 112h242.2z"></path></svg></div>
	<div class="col-sm-3"><svg aria-hidden="true" focusable="false" height="64" width="64" data-prefix="fab" data-icon="bootstrap" class="skill-icon mx-5 my-5 svg-inline--fa fa-bootstrap fa-w-18" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"><path fill="#5E3B7F" d="M333.5,201.4c0-22.1-15.6-34.3-43-34.3h-50.4v71.2h42.5C315.4,238.2,333.5,225,333.5,201.4z M517,188.6 c-9.5-30.9-10.9-68.8-9.8-98.1c1.1-30.5-22.7-58.5-54.7-58.5H123.7c-32.1,0-55.8,28.1-54.7,58.5c1,29.3-0.3,67.2-9.8,98.1 c-9.6,31-25.7,50.6-52.2,53.1v28.5c26.4,2.5,42.6,22.1,52.2,53.1c9.5,30.9,10.9,68.8,9.8,98.1c-1.1,30.5,22.7,58.5,54.7,58.5h328.7 c32.1,0,55.8-28.1,54.7-58.5c-1-29.3,0.3-67.2,9.8-98.1c9.6-31,25.7-50.6,52.1-53.1v-28.5C542.7,239.2,526.5,219.6,517,188.6z M300.2,375.1h-97.9V136.8h97.4c43.3,0,71.7,23.4,71.7,59.4c0,25.3-19.1,47.9-43.5,51.8v1.3c33.2,3.6,55.5,26.6,55.5,58.3 C383.4,349.7,352.1,375.1,300.2,375.1z M290.2,266.4h-50.1v78.4h52.3c34.2,0,52.3-13.7,52.3-39.5 C344.7,279.6,326.1,266.4,290.2,266.4z"></path></svg></div>
	<div class="col-sm-3"><svg aria-hidden="true" focusable="false" height="64" width="64" data-prefix="fab" data-icon="js-square" class="skill-icon mx-5 my-5 svg-inline--fa fa-js-square fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="#E4BA42" d="M400 32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zM243.8 381.4c0 43.6-25.6 63.5-62.9 63.5-33.7 0-53.2-17.4-63.2-38.5l34.3-20.7c6.6 11.7 12.6 21.6 27.1 21.6 13.8 0 22.6-5.4 22.6-26.5V237.7h42.1v143.7zm99.6 63.5c-39.1 0-64.4-18.6-76.7-43l34.3-19.8c9 14.7 20.8 25.6 41.5 25.6 17.4 0 28.6-8.7 28.6-20.8 0-14.4-11.4-19.5-30.7-28l-10.5-4.5c-30.4-12.9-50.5-29.2-50.5-63.5 0-31.6 24.1-55.6 61.6-55.6 26.8 0 46 9.3 59.8 33.7L368 290c-7.2-12.9-15-18-27.1-18-12.3 0-20.1 7.8-20.1 18 0 12.6 7.8 17.7 25.9 25.6l10.5 4.5c35.8 15.3 55.9 31 55.9 66.2 0 37.8-29.8 58.6-69.7 58.6z"></path></svg></div>
	<div class="col-sm-3"><svg aria-hidden="true" focusable="false" height="64" width="64" data-prefix="fab" data-icon="git-alt" class="skill-icon mx-5 my-5 svg-inline--fa fa-git-alt fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="#F15233" d="M439.55 236.05L244 40.45a28.87 28.87 0 0 0-40.81 0l-40.66 40.63 51.52 51.52c27.06-9.14 52.68 16.77 43.39 43.68l49.66 49.66c34.23-11.8 61.18 31 35.47 56.69-26.49 26.49-70.21-2.87-56-37.34L240.22 199v121.85c25.3 12.54 22.26 41.85 9.08 55a34.34 34.34 0 0 1-48.55 0c-17.57-17.6-11.07-46.91 11.25-56v-123c-20.8-8.51-24.6-30.74-18.64-45L142.57 101 8.45 235.14a28.86 28.86 0 0 0 0 40.81l195.61 195.6a28.86 28.86 0 0 0 40.8 0l194.69-194.69a28.86 28.86 0 0 0 0-40.81z"></path></svg></div>
	<div class="col-sm-3"><svg aria-hidden="true" focusable="false" height="64" width="64" data-prefix="fab" data-icon="vuejs" class="skill-icon mx-5 my-5 svg-inline--fa fa-vuejs fa-w-14" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="#3EB489" d="M356.9 64.3H280l-56 88.6-48-88.6H0L224 448 448 64.3h-91.1zm-301.2 32h53.8L224 294.5 338.4 96.3h53.8L224 384.5 55.7 96.3z"></path></svg></div>
	<div class="col-sm-3"><svg aria-hidden="true" focusable="false" data-prefix="fab" data-icon="npm" height="64" width="64" class="skill-icon mx-5 my-5 svg-inline--fa fa-npm fa-w-18" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"><path fill="#C73B3B" d="M288 288h-32v-64h32v64zm288-128v192H288v32H160v-32H0V160h576zm-416 32H32v128h64v-96h32v96h32V192zm160 0H192v160h64v-32h64V192zm224 0H352v128h64v-96h32v96h32v-96h32v96h32V192z"></path></svg></div>
	<div class="col-sm-3"><svg enable-background="new 0 0 32 32" version="1.1" viewBox="0 0 32 32" height="64" width="64" class="skill-icon mx-5 my-5" fill="#1976D2" xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><g id="_x33_0"/><g id="_x32_9"/><g id="_x32_8"/><g id="_x32_7"/><g id="_x32_6"/><g id="_x32_5"/><g id="_x32_4"/><g id="_x32_3"/><g id="_x32_2"/><g id="_x32_1"/><g id="_x32_0"/><g id="_x31_8"/><g id="_x31_7"/><g id="_x31_6"/><g id="_x31_5"/><g id="_x31_4"/><g id="_x31_3"/><g id="_x31_2"/><g id="_x31_1"/><g id="_x31_0"><path d="M27.515,6.743l-6-3.6c-0.027-0.016-0.057-0.024-0.086-0.037c-0.397-0.238-0.91-0.195-1.239,0.157l-8.419,9.021l-4.64-4.254   c-0.306-0.28-0.754-0.341-1.123-0.157L3.597,9.078C3.314,9.219,3.115,9.484,3.06,9.795s0.038,0.629,0.253,0.859L8.302,16   l-4.989,5.346c-0.215,0.23-0.309,0.549-0.253,0.859s0.255,0.576,0.537,0.717l2.411,1.206c0.142,0.071,0.295,0.105,0.447,0.105   c0.229,0,0.457-0.079,0.641-0.232l4.879-4.066l8.215,8.802c0.197,0.211,0.464,0.318,0.731,0.318c0.183,0,0.359-0.067,0.52-0.167   c0.024-0.012,0.05-0.017,0.073-0.031l6-3.6C27.815,25.077,28,24.751,28,24.4V7.6C28,7.249,27.815,6.923,27.515,6.743z    M6.317,22.046l-0.629-0.314l3.981-4.266l0.938,1.005L6.317,22.046z M20,25.602L5.688,10.268l0.599-0.299L20,22.54V25.602z    M20,19.826l-3.759-3.446L20,13.248V19.826z M20,10.644l-5.247,4.372l-1.507-1.382L20,6.398V10.644z M26,23.833l-4,2.4V5.766l4,2.4   V23.833z"/></g><g id="_x39_"/><g id="_x38_"/><g id="_x37_"/><g id="_x36_"/><g id="_x35_"/><g id="_x34_"/><g id="_x33_"/><g id="_x32_"/><g id="_x31_"/><g id="Guides"/></svg></div>
</div>

    <router-link to="/" id="home"><svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#fff" class="bi bi-house-fill" viewBox="0 0 16 16">
  <path fill-rule="evenodd" d="m8 3.293 6 6V13.5a1.5 1.5 0 0 1-1.5 1.5h-9A1.5 1.5 0 0 1 2 13.5V9.293l6-6zm5-.793V6l-2-2V2.5a.5.5 0 0 1 .5-.5h1a.5.5 0 0 1 .5.5z"/>
  <path fill-rule="evenodd" d="M7.293 1.5a1 1 0 0 1 1.414 0l6.647 6.646a.5.5 0 0 1-.708.708L8 2.207 1.354 8.854a.5.5 0 1 1-.708-.708L7.293 1.5z"/>
</svg></router-link>
</div>
    <footer>© 2022 Yaasien Salaam ALL RIGHTS RESERVED</footer>
</section>
</template>
<script>
    export default {
      name: "Resumes",
  data() {
    return {
      resumes: [
        {
          name: "National Senior Certificate",
          title: "2015 - 2019",
          id: 1,
          image: "https://i.pinimg.com/550x/d1/d9/ba/d1d9ba37625f9a1210a432731e1754f3.jpg",
          content:
            "In 2019, I matriculated at Darul Arqam Islamic High School, and within this year i started my own photography business, and with that I started my own bakery, and still worked as a barista.",
        },
        {
          name: "Arabica Coffee.co Cape Town",
          title: "2017 - 2022",
          id: 2,
          image: "https://i.pinimg.com/originals/73/e6/5e/73e65ef774b300e77aafb0dc91206647.jpg",
          content:
            "I started working for Arabica Coffee.co since they were established in 2017. I first started as an assistant for the barista, handling orders, gaining experience from the barista. In 2018 I started working for them as a barista onward",
        },
        {
          name: "Seni Silat Cape Town",
          title: "2021 - Present",
          id: 3,
          image: "data:image/png;base64,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",
          content:
            "I have studied martial arts for 10 years now, and i have been teaching as an assistant for my instructor since 2016. Started teaching on my own since may of 2021 and took over the classes since COVID hit, I teach kids and adults, on how to defend themselves.",
        },
        {
          name: "Life Choices Academy",
          title: "2021 - Present",
          id: 4,
          image: "https://us.123rf.com/450wm/tmricons/tmricons1510/tmricons151000614/45815367-html-code-icon.jpg?ver=6",
          content:
            "In 2021, I was working as a barista part time, martial arts teacher part time, and a baker. I am currently upskilling as a frontend developer, aspiring to be a fullstack. I left my bakery and still work one day of a weekend as a barista and martial arts teacher.",
        },
      ],
    };
  },
    }
</script>

<style>
#resume {
	margin-top: 100px;
}

	.skill-icon {
		background-color: #292929;
		box-shadow: rgb(38, 57, 77) 0px 20px 30px -10px;
		border-radius: 10px;
	}
	.resumes-heading h1 {
    margin-top: 2rem;
    margin-bottom: 2rem;
}
.resumes-container {
  width: 100%;
  display: flex;
  /* align-items: center; */
  justify-content: center;
  /* flex-direction: row; */
  flex-wrap: wrap;
  margin-bottom: 1rem;
  /* margin-left: 100px; */
}
.resume {
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

.resume-content {
  padding: 50px;
  display: flex;
  flex-direction: column;
}
.resume-content p {
  line-height: 25px;
  text-align: initial;
}
.resume-content img {
	height: 65px;
	width: 65px;
	border-radius: 200px;
	margin-bottom: 20px;
	box-shadow: 0 0 10px rgba(0, 0, 0, 25);
}

</style>