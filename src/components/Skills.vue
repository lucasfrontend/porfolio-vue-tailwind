<template>
    <div class="px-6 py-3">
        <div class="flex items-center justify-between">
            <h1 class="pl-2 text-2xl font-semibold text-white tracking-wider hover:underline">Titulo</h1>
            <h2 class="pr-8 pt-4 text-xs text-lightest uppercase tracking-wider hover:underline mb-3">Skills</h2>
        </div>
        <div class="w-full m-auto flex flex-wrap">
          <transition-group appear @before-enter="beforeEnter" @enter="enter">
            <div class="p-2 w-48"
                v-for="(skill, index) in skills" 
                :data-index="index" 
                :key="skill.id">
                  <v-card-skill
                      :img="skill.img"
                      :alt="skill.alt"
                      :title="skill.title"
                  />
              </div>
          </transition-group>  
      </div>    
    </div>
<!-- grilla TODOSSS
  <div class="container min-h-screen bg-dark flex items-center justify-center px-5 py-5">
    <div class="w-full max-w-2xl">
      <div class="-mx-2 flex">
        <div class="w-full px-2">
          <div class="rounded-lg shadow-sm">
            <div class="max-h-20 max-w-20 hero container max-w-screen-lg mx-auto pb-10 flex">
              <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/css.3.svg" class="mx-auto" alt="HTML Logo">
            </div>
          </div>
        </div>

        <div class="w-full px-2">
          <div class="rounded-lg shadow-sm mb-4">
            <div class="max-h-20 max-w-20 hero container max-w-screen-lg mx-auto pb-10 flex">
              <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/sass.svg" class="mx-auto" alt="HTML Logo">
            </div>
          </div>
        </div>

        <div class="w-full md:w-1/3 px-2">
          <div class="rounded-lg shadow-sm mb-4">
            <div class="max-h-20 hero container max-w-screen-lg mx-auto pb-10 flex">
              <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/tt_tailwind_logo.jpg" class="mx-auto" alt="HTML Logo">
            </div>
          </div>
        </div>

        <div class="w-full md:w-1/3 px-2">
          <div class="rounded-lg shadow-sm mb-4">
            <div class="max-h-20 hero container max-w-screen-lg mx-auto pb-10 flex">
              <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/tt_tailwind_logo.jpg" class="mx-auto" alt="HTML Logo">
            </div>
          </div>
        </div>
      </div>
      <div class="-mx-2 flex">
        <div class="w-full md:w-1/3 px-2">
          <div class="rounded-lg shadow-sm mb-4">
            <div class="max-h-40 hero container max-w-screen-lg mx-auto pb-10 flex">
              <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/react.svg" class="mx-auto" alt="HTML Logo">
            </div>
          </div>
        </div>
        <div class="w-full md:w-1/3 px-2">
          <div class="rounded-lg shadow-sm mb-4">
            <div class="max-h-40 hero container max-w-screen-lg mx-auto pb-10 flex">
              <img src="../assets/logo.png" class="mx-auto" alt="HTML Logo">
            </div>
          </div>
        </div>
        <div class="w-full md:w-1/3 px-2">
          <div class="rounded-lg shadow-sm mb-4">
            <div class="max-h-40 hero container max-w-screen-lg mx-auto pb-10 flex">
              <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/github-octocat.svg" class="mx-auto" alt="HTML Logo">
            </div>
          </div>
        </div>
        <div class="w-full md:w-1/3 px-2">
          <div class="rounded-lg shadow-sm mb-4">
            <div class="max-h-40 hero container max-w-screen-lg mx-auto pb-10 flex">
              <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/github-octocat.svg" class="mx-auto" alt="HTML Logo">
            </div>
          </div>
        </div>
      </div>

      <div class="-mx-2 flex">
        <div class="w-full md:w-1/3 px-2">
          <div class="rounded-lg shadow-sm mb-4">
            <div class="max-h-40 hero container max-w-screen-lg mx-auto pb-10 flex">
              <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/github-octocat.svg" class="mx-auto" alt="HTML Logo">
            </div>
          </div>
        </div>
        <div class="w-full md:w-1/3 px-2">
          <div class="rounded-lg shadow-sm mb-4">
            <div class="max-h-40 hero container max-w-screen-lg mx-auto pb-10 flex">
              <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/npm.svg" class="mx-auto" alt="HTML Logo">
            </div>
          </div>
        </div>
        <div class="w-full md:w-1/3 px-2">
          <div class="rounded-lg shadow-sm mb-4">
            <div class="max-h-40 hero container max-w-screen-lg mx-auto pb-10 flex">
              <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/node.svg" class="mx-auto" alt="HTML Logo">
            </div>
          </div>
        </div>
        <div class="w-full md:w-1/3 px-2">
          <div class="rounded-lg shadow-sm mb-4">
            <div class="max-h-40 hero container max-w-screen-lg mx-auto pb-10 flex">
              <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/json.svg" class="mx-auto" alt="HTML Logo">
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

-->

<!--
        <div class="max-w-5xl mx-auto px-4 sm:px-6 py-4">
          <div class="flex flex-wrap">
            <div class=" m-2 text-teal-900 bg-yellow-200 py-3 px-6 rounded">
              <p>Hello, you! ????</p>
            </div>
            <div class=" m-2 text-purple-900 bg-yellow-200 py-3 px-6 rounded">
              <p>Here is a ????</p>
            </div>
            <div class=" m-2 text-green-900 bg-yellow-200 py-3 px-6 rounded">
              <p>Tailwind  ????</p>
            </div>
            <div class=" m-2 text-teal-900 bg-yellow-200 py-3 px-6 rounded">
              <p>Hello, you! ????</p>
            </div>
            <div class="m-2 text-purple-900 bg-yellow-200 py-3 px-6 rounded">
              <p>Here is a ????</p>
            </div>
            <div class="m-2 text-green-900 bg-yellow-200 py-3 px-6 rounded">
              <p>Tailwind  ????</p>
            </div>
            <div class="m-2 text-teal-900 bg-yellow-200 py-3 px-6 rounded">
              <p>Hello, you! ????</p>
            </div>
            <div class="m-2 text-purple-900 bg-yellow-200 py-3 px-6 rounded">
              <p>Here is a ????</p>
            </div>
            <div class="m-2 text-green-900 bg-yellow-200 py-3 px-6 rounded">
              <p>Tailwind  ????</p>
            </div>
            <div class="m-2 text-teal-900 bg-yellow-200 py-3 px-6 rounded">
              <p>Hello, you! ????</p>
            </div>
            <div class="m-2 text-purple-900 bg-purple-200 py-3 px-6 rounded">
              <p>Here is a ????</p>
            </div>
            <div class="m-2 text-green-900 bg-green-200 py-3 px-6 rounded">
              <p>Tailwind  ????</p>
            </div>
            <div class="m-2 text-teal-900 bg-yellow-200 py-3 px-6 rounded">
              <p>Hello, you! ????</p>
            </div>
            <div class="m-2 text-purple-900 bg-purple-200 py-3 px-6 rounded">
              <p>Here is a ????</p>
            </div>
            <div class="m-2 text-green-900 bg-green-200 py-3 px-6 rounded">
              <p>Tailwind  ????</p>
            </div>
          </div>
        </div>    






    <div class="grid place-items-center min-h-screen">
        <div class="p-4 max-w-5xl grid gap-4 xs:grid-cols-2">
            <h1 class="text-2xl font-extrabold text-white xs:col-span-2">Lorem ipsum dolor sit amet consectetur adipisicing elit.</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. </p>
            <div class="h-16 bg-blue-500"></div>
            <div class="h-16 bg-blue-500"></div>
            <div class="h-16 bg-blue-500"></div>
            <div class="h-16 bg-blue-500"></div>
            <div class="h-16 bg-blue-500"></div>
            <div class="h-16 bg-blue-500"></div>
            <div class="h-16 bg-blue-500"></div>
            <div class="h-16 bg-blue-500"></div>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
        </div>






        <div class="flex -mx-2 mb-8">
            <div class="w-1/3 px-2">
                <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/css.3.svg" class="" alt="CSS Logo">
            </div>
            <div class="w-1/3 px-2">
                <div class="bg-grey h-12"><img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/html-5.svg" class="" alt="HTML Logo">
            </div>
            </div>
            <div class="w-1/3 px-2">
                <div class="bg-grey-light h-12">
                    <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/javascript.svg" class="" alt="CSS Logo">

                </div>
            </div>
        </div>
        <img alt="Vue logo" src="../assets/logo.png" />
        <div class="h-16 text-blue-500 flex items-center justify-center">
            <svg class="w-9" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 54 33">
                <path fill="currentColor" fill-rule="evenodd" d="M27 0c-7.2 0-11.7 3.6-13.5 10.8 2.7-3.6 5.85-4.95 9.45-4.05 2.054.513 3.522 2.004 5.147 3.653C30.744 13.09 33.808 16.2 40.5 16.2c7.2 0 11.7-3.6 13.5-10.8-2.7 3.6-5.85 4.95-9.45 4.05-2.054-.513-3.522-2.004-5.147-3.653C36.756 3.11 33.692 0 27 0zM13.5 16.2C6.3 16.2 1.8 19.8 0 27c2.7-3.6 5.85-4.95 9.45-4.05 2.054.514 3.522 2.004 5.147 3.653C17.244 29.29 20.308 32.4 27 32.4c7.2 0 11.7-3.6 13.5-10.8-2.7 3.6-5.85 4.95-9.45 4.05-2.054-.513-3.522-2.004-5.147-3.653C23.256 19.31 20.192 16.2 13.5 16.2z" clip-rule="evenodd" />
            </svg>
        </div>
        <div class="w-full lg:w-1/4">
          <img class="python-logo" src="https://cdn.worldvectorlogo.com/logos/python-5.svg" alt="Python logo">
          
          <span>express jquery pytn django boostraps</span>
          <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/html-5.svg" class="" alt="HTML Logo">
          <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/css.3.svg" class="" alt="CSS Logo">
          <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/sass.svg" class="" alt="SASS Logo">
        </div>
        <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/tt_tailwind_logo.jpg" alt="logo" class="rounded-full h-48 w-48 lg:absolute lg:pin-l lg:pin-t lg:-mt-24">
        <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/react.svg" class="" alt="React Logo">
        <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/node.svg" class="" alt="nodejs Logo">
        <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/json.svg" class="" alt="JSON Logo">
        <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/git.png" class="" alt="git Logo">
        <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/npm.svg" class="" alt="npm Logo">
        <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/github-octocat.svg" class="" alt="Github Logo">
    -->

</template>

<script>
import VCardSkill from '@/components/cards/VCardSkill.vue'
import gsap from 'gsap'

export default {
  name: 'Skills',
  components: {
    VCardSkill
  },
  data() {
    return {
        skills: [
            {
                id: 1,
                /*
                img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/html-5.svg',
                */
                img: 'https://img.shields.io/badge/-HTML5-2E303A?style=for-the-badge&logo=html5',
                title: 'Html5',
                alt: 'html logo'
            },
            {
                id: 2,
                /*
                img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/css.3.svg',
                */
                img: 'https://img.shields.io/badge/-CSS3-2E303A?style=for-the-badge&logo=css3',
                title: 'CSS',
                alt: 'CSS logo'
            },
            {
                id: 3,
                img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/sass.svg',
                title:'SASS',
                alt: 'SASS logo'
            },
            {
                id: 4,
                img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/195612/tt_tailwind_logo.jpg',
                title:'Tailwind',
                alt: 'Tailwind logo'
            },
            {
                id: 5,
                img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/sass.svg',
                title:'BOOSTRAP',
                alt: 'BOOSTRAP logo'
            },

            {
                id: 4,
                img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/react.svg',
                title: 'ReactJS',
                alt: 'REACT logo'
            },
            {
                id: 5,
                img: '../assets/logo.png',
                title: 'VUEjs',
                alt: 'VUE logo'
            },
            {
                id: 6,
                img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/node.svg',
                title: 'NODEjs',
                alt: 'NODEjs logo'
            },
            {
                id: 7,
                img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/json.svg',
                title: 'JSON',
                alt: 'JSON logo'
            },
            {
                id: 8,
                img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/git.png',
                title: 'GIT',
                alt: 'GIT logo'
            },
            {
                id: 9,
                img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/github-octocat.svg',
                title: 'Github',
                alt: 'VUE logo'
            },
            {
                id: 10,
                img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/1116997/npm.svg',
                title: 'NPM',
                alt: 'NPM logo'
            },
            {
                id: 11,
                img: 'https://cdn.worldvectorlogo.com/logos/python-5.svg',
                title: 'Python',
                alt: 'Py logo'
            },
            {
                id: 12,
                img: 'https://static.djangoproject.com/img/logo-django.42234b631760.svg',
                title: 'Django',
                alt: 'Django logo'
            },
            
            
        ]
    }
  },
  methods: {
    beforeEnter(el){
        el.style.opacity = 0;
        el.style.transform = 'transitionY(60px)'
    },
    enter(el){
        gsap.to(el, {
            opacity: 1,
            y: 0,
            duration: 1,
            delay: el.dataset.index * 0.2,
        }
      )
    }
  }
}
</script>