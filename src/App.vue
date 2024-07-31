<script setup lang="ts">
import InlineCode from './components/InlineCode.vue'
import VtuberRecs from './assets/vtuber-recs.jpg'
import JPQuizWeb from './assets/jp-quiz-web.jpg'
import Tempest from './assets/tempest.png'
import RestAPI from './assets/rest-api.png'
import ProjectCard from './components/ProjectCard.vue';
</script>

<template>
  <header>
  </header>

  <main class="min-h-screen flex justify-center lg:justify-center p-8 pt-20">
    <div class="lg:w-[44rem] flex flex-col gap-8">
      <div class="flex flex-col gap-4">
        <h2 class="text-4xl lg:text-5xl font-medium">Cyanix<span class="text-base text-gray-500 font-medium ml-2">aka
            cyan1x</span>
        </h2>

        <p class="text-lg leading-loose">
          Hey—I'm <span class="font-bold">Cyanix</span>, a trilingual <InlineCode>web developer</InlineCode>,
          <br class="sm:hidden" />
          <InlineCode>translator</InlineCode>,
          and aspiring <InlineCode>interpreter</InlineCode>.
        </p>
      </div>

      <hr class="h-1 bg-gray-200" />

      <p class="text-lg leading-relaxed">
        <span class="font-bold">As a <InlineCode class="font-bold">web developer</InlineCode>,</span>
        <br />
        most of my experience has been working with web technologies,
        writing TypeScript code,
        building frontend UIs using Vue.js and occasionally creating Discord chat bots on the backend.
      </p>
      <p class="text-lg leading-relaxed">
        <span class="font-bold">As a Japanese-English <InlineCode>translator</InlineCode>,</span>
        <br />
        I've worked on a wide variety of Japanese media, such as YouTube videos,
        checking the work of other translators for errors, giving suggestions, as well as translating entire
        scripts
        by myself.
      </p>
      <p class="text-lg leading-relaxed">
        <span class="font-bold">As an aspiring <InlineCode>interpreter</InlineCode>,</span>
        <br />
        I'm on the lookout for opportunities where I can apply my skills as a native-level Japanese speaker,
        Japanese-English translator, and front-end web developer.
      </p>

      <p class="italic">You can find examples of my work below.</p>

      <hr class="h-1 bg-gray-200" />

      <h2 class="text-2xl font-bold">Projects</h2>
      <ProjectCard title="rest-api" :imgSrc="RestAPI" flavorText="Read about it at"
        link="https://github.com/cyan1x/rest-api/">
        <div class="flex flex-col gap-1">
          <p class="text-sm text-gray-400">日本語解説あり</p>
          <p>A full-featured REST API backend for a (hypothetical) mobile app that tracks runs, such as sprints and
            marathons.</p>
          <p>Check the GitHub repository for a more detailed description in both English and Japanese.</p>
        </div>
        <template #tech-stack>
          <div>
            <table>
              <tr>
                <th class="border-2 border-gray-300 p-2" colspan="2">Teck stack</th>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">Framework</td>
                <td class="border-2 border-gray-300 p-2">Express.js</td>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">Database</td>
                <td class="border-2 border-gray-300 p-2">PostgreSQL</td>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">ORM</td>
                <td class="border-2 border-gray-300 p-2">TypeORM</td>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">Testing</td>
                <td class="border-2 border-gray-300 p-2">Chai, Mocha, Sinon.JS, Faker, Supertest</td>
              </tr>
            </table>
          </div>
        </template>
      </ProjectCard>
      <ProjectCard title="Tempest" :imgSrc="Tempest" flavorText="Under construction">
        <div class="flex flex-col gap-1">
          <p>A highly customizable desktop application for managing videos and tracking total time watched.</p>
          <p>I wrote the file browser UI from scratch, using elements from daisyUI.</p>
        </div>
        <template #tech-stack>
          <div>
            <table>
              <tr>
                <th class="border-2 border-gray-300 p-2" colspan="2">Teck stack</th>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">Framework</td>
                <td class="border-2 border-gray-300 p-2"><a href="https://www.electronjs.org/">Electron</a>, <a
                    href="https://vuejs.org/">Vue.js</a></td>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">Styling</td>
                <td class="border-2 border-gray-300 p-2"><a href="https://tailwindcss.com/">Tailwind CSS</a></td>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">Components</td>
                <td class="border-2 border-gray-300 p-2"><a href="https://daisyui.com/">daisyUI</a></td>
              </tr>
            </table>
          </div>
        </template>
      </ProjectCard>
      <ProjectCard title="vtuber-recs" :imgSrc="VtuberRecs" flavorText="Check it out at"
        link="https://vtuber-recs.netlify.app/">
        <div class="flex flex-col gap-1">
          <p>A simple recommendation list for any Japanese learner/speaker wanting to get into VTubers, complete with
            descriptions,
            tags and links for each.</p>
          <p>I will be adding more entries over time, as well as embedded YouTube clips.</p>
        </div>
        <template #tech-stack>
          <div>
            <table>
              <tr>
                <th class="border-2 border-gray-300 p-2" colspan="2">Teck stack</th>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">Framework</td>
                <td class="border-2 border-gray-300 p-2"><a href="https://vuejs.org/">Vue.js</a></td>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">Styling</td>
                <td class="border-2 border-gray-300 p-2">Plain CSS</td>
              </tr>
            </table>
          </div>
        </template>
      </ProjectCard>
      <ProjectCard title="jp-quiz-web" :imgSrc="JPQuizWeb" flavorText="Play it at" link="https://jp-quiz.netlify.app/">
        <div class="flex flex-col gap-1">
          <p>Test your Japanese (or English!) skills on this <a class="link"
              href="https://monkeytype.com/">Monkeytype</a>-inspired quiz game.</p>
          <p class="italic text-gray-500">Still thinking of ways to make this more fun. Let me know if you have any
            ideas.</p>
        </div>
        <template #tech-stack>
          <div>
            <table>
              <tr>
                <th class="border-2 border-gray-300 p-2" colspan="2">Teck stack</th>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">Framework</td>
                <td class="border-2 border-gray-300 p-2"><a href="https://vuejs.org/">Vue.js</a></td>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">Styling</td>
                <td class="border-2 border-gray-300 p-2"><a href="https://tailwindcss.com/">Tailwind CSS</a></td>
              </tr>
            </table>
          </div>
        </template>
      </ProjectCard>
      <ProjectCard title="This website" flavorText="You can find the code at"
        link="https://github.com/cyan1x/portfolio/">
        A minimalistic portfolio website, designed by yours truly.
        <template #tech-stack>
          <div>
            <table>
              <tr>
                <th class="border-2 border-gray-300 p-2" colspan="2">Teck stack</th>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">Framework</td>
                <td class="border-2 border-gray-300 p-2"><a href="https://vuejs.org/">Vue.js</a></td>
              </tr>
              <tr>
                <td class="border-2 border-gray-300 p-2">Styling</td>
                <td class="border-2 border-gray-300 p-2"><a href="https://tailwindcss.com/">Tailwind CSS</a></td>
              </tr>
            </table>
          </div>
        </template>
      </ProjectCard>
    </div>
  </main>
</template>
