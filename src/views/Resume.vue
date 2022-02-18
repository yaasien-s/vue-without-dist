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
              <div class="col-sm-10 resume-name">
                <h2>{{ resume.name }}</h2>
              </div>
            </div>
            <p>{{ resume.content }}</p>
            <cite>{{ resume.title }}</cite>
          </div>
        </div>
      </div>

      <h1>Technical Skills</h1>
      <div class="row text-align-center skill-icons">
        <div class="col-sm-3">
          <div title="HTML-5"><svg aria-hidden="true" focusable="false" height="75" width="75" data-prefix="fab"
              data-icon="html5" class="skill-icon mx-5 my-5 svg-inline--fa fa-html5 fa-w-12" role="img"
              xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512">
              <path fill="#E44D26"
                d="M0 32l34.9 395.8L191.5 480l157.6-52.2L384 32H0zm308.2 127.9H124.4l4.1 49.4h175.6l-13.6 148.4-97.9 27v.3h-1.1l-98.7-27.3-6-75.8h47.7L138 320l53.5 14.5 53.7-14.5 6-62.2H84.3L71.5 112.2h241.1l-4.4 47.7z">
              </path>
            </svg></div>
          <div title="CSS-3"><svg aria-hidden="true" focusable="false" height="75" width="75" data-prefix="fab"
              data-icon="css3-alt" class="skill-icon mx-5 my-5 svg-inline--fa fa-css3-alt fa-w-12" role="img"
              xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512">
              <path fill="#347DC6"
                d="M0 32l34.9 395.8L192 480l157.1-52.2L384 32H0zm313.1 80l-4.8 47.3L193 208.6l-.3.1h111.5l-12.8 146.6-98.2 28.7-98.8-29.2-6.4-73.9h48.9l3.2 38.3 52.6 13.3 54.7-15.4 3.7-61.6-166.3-.5v-.1l-.2.1-3.6-46.3L193.1 162l6.5-2.7H76.7L70.9 112h242.2z">
              </path>
            </svg></div>
        </div>
        <div class="col-sm-3">
          <div title="Bootstrap"><svg aria-hidden="true" focusable="false" height="75" width="75" data-prefix="fab"
              data-icon="bootstrap" class="skill-icon mx-5 my-5 svg-inline--fa fa-bootstrap fa-w-18" role="img"
              xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
              <path fill="#5E3B7F"
                d="M333.5,201.4c0-22.1-15.6-34.3-43-34.3h-50.4v71.2h42.5C315.4,238.2,333.5,225,333.5,201.4z M517,188.6 c-9.5-30.9-10.9-68.8-9.8-98.1c1.1-30.5-22.7-58.5-54.7-58.5H123.7c-32.1,0-55.8,28.1-54.7,58.5c1,29.3-0.3,67.2-9.8,98.1 c-9.6,31-25.7,50.6-52.2,53.1v28.5c26.4,2.5,42.6,22.1,52.2,53.1c9.5,30.9,10.9,68.8,9.8,98.1c-1.1,30.5,22.7,58.5,54.7,58.5h328.7 c32.1,0,55.8-28.1,54.7-58.5c-1-29.3,0.3-67.2,9.8-98.1c9.6-31,25.7-50.6,52.1-53.1v-28.5C542.7,239.2,526.5,219.6,517,188.6z M300.2,375.1h-97.9V136.8h97.4c43.3,0,71.7,23.4,71.7,59.4c0,25.3-19.1,47.9-43.5,51.8v1.3c33.2,3.6,55.5,26.6,55.5,58.3 C383.4,349.7,352.1,375.1,300.2,375.1z M290.2,266.4h-50.1v78.4h52.3c34.2,0,52.3-13.7,52.3-39.5 C344.7,279.6,326.1,266.4,290.2,266.4z">
              </path>
            </svg></div>
          <div title="JavaScript"><svg aria-hidden="true" focusable="false" height="75" width="75" data-prefix="fab"
              data-icon="js-square" class="skill-icon mx-5 my-5 svg-inline--fa fa-js-square fa-w-14" role="img"
              xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
              <path fill="#E4BA42"
                d="M400 32H48C21.5 32 0 53.5 0 80v352c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V80c0-26.5-21.5-48-48-48zM243.8 381.4c0 43.6-25.6 63.5-62.9 63.5-33.7 0-53.2-17.4-63.2-38.5l34.3-20.7c6.6 11.7 12.6 21.6 27.1 21.6 13.8 0 22.6-5.4 22.6-26.5V237.7h42.1v143.7zm99.6 63.5c-39.1 0-64.4-18.6-76.7-43l34.3-19.8c9 14.7 20.8 25.6 41.5 25.6 17.4 0 28.6-8.7 28.6-20.8 0-14.4-11.4-19.5-30.7-28l-10.5-4.5c-30.4-12.9-50.5-29.2-50.5-63.5 0-31.6 24.1-55.6 61.6-55.6 26.8 0 46 9.3 59.8 33.7L368 290c-7.2-12.9-15-18-27.1-18-12.3 0-20.1 7.8-20.1 18 0 12.6 7.8 17.7 25.9 25.6l10.5 4.5c35.8 15.3 55.9 31 55.9 66.2 0 37.8-29.8 58.6-69.7 58.6z">
              </path>
            </svg></div>
        </div>
        <div class="col-sm-3">
          <div title="Wordpress"><svg viewBox="0 0 512 512" xmlns="http://www.w3.org/2000/svg" height="75" width="75" class="skill-icon mx-5 my-5 svg-inline--fa fa-wordpress fa-w-14" fill="#21759B">
              <path
                d="M61.7 169.4l101.5 278C92.2 413 43.3 340.2 43.3 256c0-30.9 6.6-60.1 18.4-86.6zm337.9 75.9c0-26.3-9.4-44.5-17.5-58.7-10.8-17.5-20.9-32.4-20.9-49.9 0-19.6 14.8-37.8 35.7-37.8.9 0 1.8.1 2.8.2-37.9-34.7-88.3-55.9-143.7-55.9-74.3 0-139.7 38.1-177.8 95.9 5 .2 9.7.3 13.7.3 22.2 0 56.7-2.7 56.7-2.7 11.5-.7 12.8 16.2 1.4 17.5 0 0-11.5 1.3-24.3 2l77.5 230.4L249.8 247l-33.1-90.8c-11.5-.7-22.3-2-22.3-2-11.5-.7-10.1-18.2 1.3-17.5 0 0 35.1 2.7 56 2.7 22.2 0 56.7-2.7 56.7-2.7 11.5-.7 12.8 16.2 1.4 17.5 0 0-11.5 1.3-24.3 2l76.9 228.7 21.2-70.9c9-29.4 16-50.5 16-68.7zm-139.9 29.3l-63.8 185.5c19.1 5.6 39.2 8.7 60.1 8.7 24.8 0 48.5-4.3 70.6-12.1-.6-.9-1.1-1.9-1.5-2.9l-65.4-179.2zm183-120.7c.9 6.8 1.4 14 1.4 21.9 0 21.6-4 45.8-16.2 76.2l-65 187.9C426.2 403 468.7 334.5 468.7 256c0-37-9.4-71.8-26-102.1zM504 256c0 136.8-111.3 248-248 248C119.2 504 8 392.7 8 256 8 119.2 119.2 8 256 8c136.7 0 248 111.2 248 248zm-11.4 0c0-130.5-106.2-236.6-236.6-236.6C125.5 19.4 19.4 125.5 19.4 256S125.6 492.6 256 492.6c130.5 0 236.6-106.1 236.6-236.6z" />
              </svg></div>
          <div title="Vue JS"><svg aria-hidden="true" focusable="false" height="75" width="75" data-prefix="fab"
              data-icon="vuejs" class="skill-icon mx-5 my-5 svg-inline--fa fa-vuejs fa-w-14" role="img"
              xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
              <path fill="#3EB489"
                d="M356.9 64.3H280l-56 88.6-48-88.6H0L224 448 448 64.3h-91.1zm-301.2 32h53.8L224 294.5 338.4 96.3h53.8L224 384.5 55.7 96.3z">
              </path>
            </svg></div>
        </div>
        <div class="col-sm-3">
          <div title="MySQL"><svg class="skill-icon mx-5 my-5 svg-inline--fa fa-mysql fa-w-14" width="75" height="75"
              viewBox="-18.458 -22.75 191.151 191.151" xmlns="http://www.w3.org/2000/svg">
              <path d="M-18.458 6.58h191.151v132.49H-18.458V6.58z" fill="none" />
              <path
                d="M40.054 113.583h-5.175c-.183-8.735-.687-16.947-1.511-24.642h-.046l-7.879 24.642h-3.94l-7.832-24.642h-.045c-.581 7.388-.947 15.602-1.099 24.642H7.81c.304-10.993 1.068-21.299 2.289-30.919h6.414l7.465 22.719h.046l7.511-22.719h6.137c1.344 11.268 2.138 21.575 2.382 30.919M62.497 90.771c-2.107 11.434-4.887 19.742-8.337 24.928-2.688 3.992-5.633 5.99-8.84 5.99-.855 0-1.91-.258-3.16-.77v-2.757c.611.088 1.328.138 2.152.138 1.498 0 2.702-.412 3.62-1.238 1.098-1.006 1.647-2.137 1.647-3.388 0-.858-.428-2.612-1.282-5.268L42.618 90.77h5.084l4.076 13.19c.916 2.995 1.298 5.086 1.145 6.277 2.229-5.953 3.786-12.444 4.673-19.468h4.901v.002z"
                fill="#5d87a1" />
              <path
                d="M131.382 113.583h-14.7V82.664h4.945v27.113h9.755v3.806zM112.834 114.33l-5.684-2.805c.504-.414.986-.862 1.42-1.381 2.416-2.838 3.621-7.035 3.621-12.594 0-10.229-4.014-15.346-12.045-15.346-3.938 0-7.01 1.298-9.207 3.895-2.414 2.84-3.619 7.022-3.619 12.551 0 5.435 1.068 9.422 3.205 11.951 1.955 2.291 4.902 3.438 8.843 3.438 1.47 0 2.819-.18 4.048-.543l7.4 4.308 2.018-3.474zm-18.413-6.934c-1.252-2.014-1.878-5.248-1.878-9.707 0-7.785 2.365-11.682 7.1-11.682 2.475 0 4.289.932 5.449 2.792 1.25 2.017 1.879 5.222 1.879 9.619 0 7.849-2.367 11.774-7.099 11.774-2.476.001-4.29-.928-5.451-2.796M85.165 105.013c0 2.622-.962 4.773-2.884 6.458-1.924 1.678-4.504 2.519-7.737 2.519-3.024 0-5.956-.966-8.794-2.888l1.329-2.655c2.442 1.223 4.653 1.831 6.638 1.831 1.863 0 3.319-.413 4.375-1.232 1.055-.822 1.684-1.975 1.684-3.433 0-1.837-1.281-3.407-3.631-4.722-2.167-1.19-6.501-3.678-6.501-3.678-2.349-1.712-3.525-3.55-3.525-6.578 0-2.506.877-4.529 2.632-6.068 1.757-1.545 4.024-2.315 6.803-2.315 2.87 0 5.479.769 7.829 2.291l-1.192 2.656c-2.01-.854-3.994-1.281-5.951-1.281-1.585 0-2.809.381-3.66 1.146-.858.762-1.387 1.737-1.387 2.933 0 1.828 1.308 3.418 3.722 4.759 2.196 1.192 6.638 3.723 6.638 3.723 2.409 1.709 3.612 3.53 3.612 6.534"
                fill="#f8981d" />
              <path
                d="M137.59 72.308c-2.99-.076-5.305.225-7.248 1.047-.561.224-1.453.224-1.531.933.303.3.338.784.601 1.198.448.747 1.229 1.752 1.942 2.276.783.6 1.569 1.194 2.393 1.717 1.453.899 3.1 1.422 4.516 2.318.825.521 1.645 1.195 2.471 1.756.406.299.666.784 1.193.971v-.114c-.264-.336-.339-.822-.598-1.196l-1.122-1.082c-1.084-1.456-2.431-2.727-3.884-3.771-1.196-.824-3.812-1.944-4.297-3.322l-.076-.076c.822-.077 1.797-.375 2.578-.604 1.271-.335 2.43-.259 3.734-.594.6-.15 1.195-.338 1.797-.523v-.337c-.676-.673-1.158-1.567-1.869-2.203-1.902-1.643-3.998-3.25-6.164-4.595-1.16-.749-2.652-1.231-3.887-1.868-.445-.225-1.195-.336-1.457-.71-.67-.822-1.047-1.904-1.533-2.877-1.08-2.053-2.129-4.331-3.061-6.502-.674-1.456-1.084-2.91-1.906-4.257-3.85-6.35-8.031-10.196-14.457-13.971-1.381-.786-3.024-1.121-4.779-1.533l-2.803-.148c-.598-.262-1.197-.973-1.719-1.309-2.132-1.344-7.621-4.257-9.189-.411-1.01 2.431 1.494 4.821 2.354 6.054.635.856 1.458 1.83 1.902 2.802.263.635.337 1.309.6 1.98.598 1.644 1.157 3.473 1.943 5.007.41.782.857 1.604 1.381 2.312.3.414.822.597.936 1.272-.521.744-.562 1.867-.861 2.801-1.344 4.221-.819 9.45 1.086 12.552.596.934 2.018 2.99 3.92 2.202 1.684-.672 1.311-2.801 1.795-4.668.111-.451.038-.747.262-1.043v.073c.521 1.045 1.047 2.052 1.53 3.1 1.159 1.829 3.177 3.735 4.858 5.002.895.676 1.604 1.832 2.725 2.245V74.1h-.074c-.227-.335-.559-.485-.857-.745-.674-.673-1.42-1.495-1.943-2.241-1.566-2.093-2.952-4.41-4.182-6.801-.602-1.16-1.121-2.428-1.606-3.586-.226-.447-.226-1.121-.601-1.346-.562.821-1.381 1.532-1.791 2.538-.711 1.609-.785 3.588-1.049 5.646l-.147.072c-1.19-.299-1.604-1.53-2.056-2.575-1.119-2.654-1.307-6.914-.336-9.976.26-.783 1.385-3.249.936-3.995-.225-.715-.973-1.122-1.383-1.685-.482-.708-1.01-1.604-1.346-2.39-.896-2.091-1.347-4.408-2.312-6.498-.451-.974-1.234-1.982-1.868-2.879-.712-1.008-1.495-1.718-2.058-2.913-.186-.411-.447-1.083-.148-1.53.073-.3.225-.412.523-.487.484-.409 1.867.111 2.352.336 1.385.56 2.543 1.083 3.699 1.867.523.375 1.084 1.085 1.755 1.272h.786c1.193.26 2.538.072 3.661.41 1.979.636 3.772 1.569 5.38 2.576 4.893 3.103 8.928 7.512 11.652 12.778.447.858.637 1.644 1.045 2.539.787 1.832 1.76 3.7 2.541 5.493.785 1.755 1.533 3.547 2.654 5.005.559.784 2.805 1.195 3.812 1.606.745.335 1.905.633 2.577 1.044 1.271.783 2.537 1.682 3.732 2.543.595.448 2.465 1.382 2.576 2.13M99.484 39.844a5.82 5.82 0 0 0-1.529.188v.075h.072c.301.597.824 1.011 1.197 1.532.301.599.562 1.193.857 1.791l.072-.074c.527-.373.789-.971.789-1.868-.227-.264-.262-.522-.451-.784-.22-.374-.705-.56-1.007-.86"
                fill="#5d87a1" />
              <path
                d="M141.148 113.578h.774v-3.788h-1.161l-.947 2.585-1.029-2.585h-1.118v3.788h.731v-2.882h.041l1.078 2.882h.557l1.074-2.882v2.882zm-6.235 0h.819v-3.146h1.072v-.643h-3.008v.643h1.115l.002 3.146z"
                fill="#f8981d" /></svg></div>
          <div title="Node JS"><svg class="skill-icon mx-5 my-5 svg-inline--fa fa-nodejs fa-w-14" width="75" height="75"
              viewBox="0 0 256 282" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMinYMin meet">
              <g fill="#8CC84B">
                <path
                  d="M116.504 3.58c6.962-3.985 16.03-4.003 22.986 0 34.995 19.774 70.001 39.517 104.99 59.303 6.581 3.707 10.983 11.031 10.916 18.614v118.968c.049 7.897-4.788 15.396-11.731 19.019-34.88 19.665-69.742 39.354-104.616 59.019-7.106 4.063-16.356 3.75-23.24-.646-10.457-6.062-20.932-12.094-31.39-18.15-2.137-1.274-4.546-2.288-6.055-4.36 1.334-1.798 3.719-2.022 5.657-2.807 4.365-1.388 8.374-3.616 12.384-5.778 1.014-.694 2.252-.428 3.224.193 8.942 5.127 17.805 10.403 26.777 15.481 1.914 1.105 3.852-.362 5.488-1.274 34.228-19.345 68.498-38.617 102.72-57.968 1.268-.61 1.969-1.956 1.866-3.345.024-39.245.006-78.497.012-117.742.145-1.576-.767-3.025-2.192-3.67-34.759-19.575-69.5-39.18-104.253-58.76a3.621 3.621 0 0 0-4.094-.006C91.2 39.257 56.465 58.88 21.712 78.454c-1.42.646-2.373 2.071-2.204 3.653.006 39.245 0 78.497 0 117.748a3.329 3.329 0 0 0 1.89 3.303c9.274 5.259 18.56 10.481 27.84 15.722 5.228 2.814 11.647 4.486 17.407 2.33 5.083-1.823 8.646-7.01 8.549-12.407.048-39.016-.024-78.038.036-117.048-.127-1.732 1.516-3.163 3.2-3 4.456-.03 8.918-.06 13.374.012 1.86-.042 3.14 1.823 2.91 3.568-.018 39.263.048 78.527-.03 117.79.012 10.464-4.287 21.85-13.966 26.97-11.924 6.177-26.662 4.867-38.442-1.056-10.198-5.09-19.93-11.097-29.947-16.55C5.368 215.886.555 208.357.604 200.466V81.497c-.073-7.74 4.504-15.197 11.29-18.85C46.768 42.966 81.636 23.27 116.504 3.58z" />
                <path
                  d="M146.928 85.99c15.21-.979 31.493-.58 45.18 6.913 10.597 5.742 16.472 17.793 16.659 29.566-.296 1.588-1.956 2.464-3.472 2.355-4.413-.006-8.827.06-13.24-.03-1.872.072-2.96-1.654-3.195-3.309-1.268-5.633-4.34-11.212-9.642-13.929-8.139-4.075-17.576-3.87-26.451-3.785-6.479.344-13.446.905-18.935 4.715-4.214 2.886-5.494 8.712-3.99 13.404 1.418 3.369 5.307 4.456 8.489 5.458 18.33 4.794 37.754 4.317 55.734 10.626 7.444 2.572 14.726 7.572 17.274 15.366 3.333 10.446 1.872 22.932-5.56 31.318-6.027 6.901-14.805 10.657-23.56 12.697-11.647 2.597-23.734 2.663-35.562 1.51-11.122-1.268-22.696-4.19-31.282-11.768-7.342-6.375-10.928-16.308-10.572-25.895.085-1.619 1.697-2.748 3.248-2.615 4.444-.036 8.888-.048 13.332.006 1.775-.127 3.091 1.407 3.182 3.08.82 5.367 2.837 11 7.517 14.182 9.032 5.827 20.365 5.428 30.707 5.591 8.568-.38 18.186-.495 25.178-6.158 3.689-3.23 4.782-8.634 3.785-13.283-1.08-3.925-5.186-5.754-8.712-6.95-18.095-5.724-37.736-3.647-55.656-10.12-7.275-2.571-14.31-7.432-17.105-14.906-3.9-10.578-2.113-23.662 6.098-31.765 8.006-8.06 19.563-11.164 30.551-12.275z" />
              </g>
            </svg></div>
        </div>
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
    name: "Resumes",
    data() {
      return {
        resumes: [{
            name: "National Senior Certificate",
            title: "2015 - 2019",
            id: 1,
            image: "https://i.pinimg.com/550x/d1/d9/ba/d1d9ba37625f9a1210a432731e1754f3.jpg",
            content: "In 2019, I matriculated at Darul Arqam Islamic High School, and within this year i started my own photography business, and with that I started my own bakery, and still worked as a barista.",
          },
          {
            name: "Arabica Coffee.co Cape Town",
            title: "2017 - 2022",
            id: 2,
            image: "https://i.pinimg.com/originals/73/e6/5e/73e65ef774b300e77aafb0dc91206647.jpg",
            content: "I started working for Arabica Coffee.co since they were established in 2017. I first started as an assistant for the barista, handling orders, gaining experience from the barista. In 2018 I started working for them as a barista onward",
          },
          {
            name: "Seni Silat Cape Town",
            title: "2021 - Present",
            id: 3,
            image: "data:image/png;base64,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",
            content: "I have studied martial arts for 10 years now, and i have been teaching as an assistant for my instructor since 2016. Started teaching on my own since may of 2021 and took over the classes since COVID hit, I teach kids and adults, on how to defend themselves.",
          },
          {
            name: "Life Choices Academy",
            title: "2021 - Present",
            id: 4,
            image: "https://us.123rf.com/450wm/tmricons/tmricons1510/tmricons151000614/45815367-html-code-icon.jpg?ver=6",
            content: "In 2021, I was working as a barista part time, martial arts teacher part time, and a baker. I am currently upskilling as a frontend developer, aspiring to be a fullstack. I left my bakery and still work one day of a weekend as a barista and martial arts teacher.",
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
    background-color: #2b2b26;
    box-shadow: rgb(38, 57, 77) 0px 20px 30px -10px;
    border-radius: 10px;
    margin-left: auto !important;
    margin-right: auto !important;
  }

  div[title] {
    position: relative;
  }

  div[title]:hover:after {
    content: attr(title);
    border-radius: 5px;
    transition: 0.3s;
    font-size: 1.2rem;
    font-weight: 600;
    color: #568259;
    background: #2b2b26;
    padding: 5px;
    position: absolute;
    transform: translate(-50%, 100%);
    left: 50%;
    top: 50%;
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

  .resume-name {
    text-align: initial;
  }

  .resume-content {
    padding: 50px;
    display: flex;
    flex-direction: column;
  }

  .resume-content p {
    line-height: 25px;
    width: 65vw;
    margin-left: 40px;
    text-align: initial;
  }

  .resume-content img {
    height: 75px;
    width: 75px;
    border-radius: 200px;
    margin-bottom: 30px;
    margin-top: -17px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 25);
  }

  @media (max-width: 770px) {
    .resume-name {
      text-align: center;
    }

    .resume-content p {
      width: auto;
      margin-left: auto;
    }
  }

  @media (max-width: 580px) {
    .skill-icon {
      width: 48px;
      height: 48px;
      border-radius: 5px;
    }

    .skill-icons>* {
      width: 50% !important;
      margin-left: auto;
      margin-right: auto;
    }
  }
</style>