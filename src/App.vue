<script setup lang="ts">
import InlineCode from './components/InlineCode.vue'
import VtuberRecs from './assets/vtuber-recs.jpg'
import JPQuizWeb from './assets/jp-quiz-web.jpg'
import ProjectCard from './components/ProjectCard.vue';
</script>

<template>
  <header>
  </header>

  <main class="min-h-screen flex justify-center lg:justify-start lg:pl-32 p-8 pt-20">
    <div class="lg:w-[44rem] flex flex-col gap-8">
      <div class="flex flex-col gap-4">
        <h2 class="text-4xl lg:text-5xl font-medium">Cyanix<span class="text-base text-gray-500 font-medium ml-2">aka
            cyan1x</span>
        </h2>

        <p class="text-lg leading-loose">
          Hey—I'm <span class="font-bold">Cyanix</span>, a <InlineCode>web developer</InlineCode>
          <br class="sm:hidden" />
          and a Japanese to English <InlineCode>translator</InlineCode>.
        </p>
      </div>

      <hr class="h-0.5 bg-gray-200" />

      <p class="text-lg leading-relaxed">
        <span class="font-bold">As a <InlineCode class="font-bold">web developer</InlineCode>,</span>
        <br />
        most of my experience has been working with web technologies,
        writing TypeScript code,
        building frontend UIs using Vue.js and creating Discord chatbots on the backend.
      </p>
      <p class="text-lg leading-relaxed">
        <span class="font-bold">As a <InlineCode>translator</InlineCode>,</span>
        <br />
        I've worked on a wide variety of Japanese media, mainly anime,
        checking the work of other translators for errors, giving suggestions, as well as translating entire
        scripts
        by myself.
      </p>

      <hr class="h-0.5 bg-gray-200" />

      <h2 class="text-2xl font-bold">Projects</h2>
      <ProjectCard title="vtuber-recs" :imgSrc="VtuberRecs" flavorText="Check it out at"
        link="https://vtuber-recs.netlify.app/">
        A recommendation list for any Japanese learner/speaker wanting to get into VTubers, complete with descriptions,
        tags and links for each.
        <template #tech-stack>
          <div>
            <table class="border-collapse">
              <tr>
                <th class="border-2 p-2" colspan="2">Teck stack</th>
              </tr>
              <tr>
                <td class="border-2 p-2">Framework</td>
                <td class="border-2 p-2"><a href="https://vuejs.org/">Vue.js</a></td>
              </tr>
              <tr>
                <td class="border-2 p-2">Styling</td>
                <td class="border-2 p-2"><a href="https://tailwindcss.com/">Tailwind CSS</a></td>
              </tr>
            </table>
          </div>
        </template>
      </ProjectCard>
      <ProjectCard title="jp-quiz-web" :imgSrc="JPQuizWeb" flavorText="Try it at" link="https://jp-quiz.netlify.app/">
        Test your Japanese (or English!) skills on this fast-paced, <a class="link"
          href="https://monkeytype.com/">Monkeytype</a>-inspired quiz game.
      </ProjectCard>
    </div>
  </main>
</template>
