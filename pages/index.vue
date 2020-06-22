<template>
  <div class="container">
    <div>
      <section class="min-h-screen flex items-center">
        <h1 style="font-size: 100px;">Hi I'm Pau, a Full-stack Web Developer Freelance</h1>
      </section>

      <Slide
        v-for="(slide, index) in slides"
        :key="index"
        v-bind:title="slide.title"
        v-bind:subtitle="slide.subtitle"
        v-bind:content="slide.content"
        v-bind:small="slide.small"
      />

      <D3FullStack />

      <section class="my-48 text-center">
        <div class="links">
          <a
            href="https://www.linkedin.com/in/pau-penin/"
            target="_blank"
            rel="noopener noreferrer"
            class="button--green"
          >LinkedIn</a>
          <a
            href="https://github.com/paupenin/"
            target="_blank"
            rel="noopener noreferrer"
            class="button--green"
          >GitHub</a>
          <a
            href="mailto:hi@paupenin.com"
            target="_blank"
            rel="noopener noreferrer"
            class="button--green"
          >Email</a>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import D3FullStack from '~/components/D3FullStack.vue'
import Slide from '~/components/Slide.vue'

export default {
  components: {
    Slide,
    D3FullStack
  },

  data() {
    return {
      'slides': [
        // Professional Experience
        {
          'title': "My Professional Experience",
          'small': true,
        },
        {
          'subtitle': "Front-end Web Developer",
          'content': [
            "In 2010, after finishing development studies, I joined a small development company in Barcelona as an intern.",
            "What should be a 3-month internship became a 5 years full-time job where I acquired tons of experience.",
            "Skills: HTML, CSS, Bootstrap, JS, jQuery, AJAX and BackboneJS",
          ]
        },
        {
          'subtitle': "Back-end Developer",
          'content': [
            "After 3 years working as a Front-end web developer, my mentor left the company and I had the opportunity to replace him as a Back-end developer.",
            "Skills: PHP, MySQL, Oracle, NodeJS, MongoDB, SphinxQL, API SOAP and API REST",
          ]
        },
        {
          'subtitle': "Dev-ops and System Admin",
          'content': [
            "Working in a small company is mandatory to go out of your comfort area to provide solutions that can be very specialized, which allows you to improve your skills on other topics.",
            "During some period I had to integrate the systems, automatizations, and servers for all customers.",
            "Skills: Ubuntu Server, Apache, NGINX, Jenkins, and GIT",
          ]
        },
        {
          'subtitle': "Team Leader, Project Manager and Digital Analyst",
          'content': [
            "Besides my job as a Back-end developer I had to take care of some interns who I mentored and led for the next 2 years to do my previous Front-end development tasks.",
            "At the same time, responsibilities incremented by having close contact with customers, budgeting, and proposing solutions.",
            "Skills: Analysis, Management, Agile, and SCRUM",
          ]
        },
        {
          'subtitle': "Freelance Full-stack developer",
          'content': [
            "In 2015 the company started a process to be acquired and integrated as the development department for one of my assigned customers.",
            "I had the feeling that I reached the ceiling on that position and that I could contribute and grow by becoming a freelancer, a gut feeling that proved right soon when I started to collaborate with different customers and agencies.",
            "Skills: HTML5, CSS3, Laravel, TailwindCSS, MSQL, WordPress, Prestashop, Docker, React, Angular, Vue, Gulp and WebPack",
          ]
        },
        // Motivates
        {
          'title': "What motivates me",
          'content': [
            "My professional growth path brought me to a point where I can choose projects, that makes me wonder what I would like to achieve and in which direction I may be interested to grow.",
            "I already have very good experiencie working for organizations like: Generalitat de Catalunya, Colegi de Notaris de Catalunya, Centres Esportius per a Tothom 10, Nutrición sin fronteras and Futbol Club Barcelona.",
            "But, I want new challenges, better customers and to be part of a great team; Elkanodata matches all these.",
          ],
        },
        // Projects
        {
          'title': "Relevant Portfolio",
          'small': true,
        },
        {
          'subtitle': "Intranet Colegi de Notaris de Catalunya",
          'content': [
            "Colegi de Notaris de Catalunya started the digitalization of all documents stored on their archives.",
            "I developed a platform that consisted of a web app (Front-end) and a PHP API (Back-end) to search and display any digital documents on CNC.",
            "This platform was planned to be integrated with the existing IBM Lotus Notes Server to access documents and privileges.",
            "The biggest challenge of the project was time performance on wild card searches.",
            "The project used Lotus Notes which was too slow performing searches on Data Base of over a million documents.",
            "To solve this I had to develop a microservice to synchronize the data recursively and store it on a much more efficient wild card search Data Base.",
            "This project makes me proud because I achieved to search any text on over a million documents with an average response of 200ms.",
            "I think that the experience of working with big amounts of data, which may be stored on legacy platforms, can help to create stunning and performant presentations for your customers.",
          ]
        },
        {
          'subtitle': "Automatic Trans",
          'content': [
            "Automatic Trans, now called AT Language Solutions, is a translation service company.",
            "I participated in the development of different web tools that were integrated with different machine learning translation engines.",
            "These tools were used to manage the translation engines, workers, and most importantly, a platform where human translators were checking the automated translations by the translation engines and fixing them. Then the proper translation would be sent to the final document and back to the translation engine for improvement of the automatized translation quality.",
            "These tools were interacting with a huge user base. I can provide my experience with a core business tool that had to deal with high traffic, performance issues, and multiple integrations.",
          ]
        },
        {
          'subtitle': "Full-stack Web Developer Freelance",
          'content': [
            "Even if this is not a single project as the previous ones I had the opportunity to participate in very exciting projects as Freelancer during the last 5 years.",
            "Each of the projects has different complexity and challenges but they allowed me to improve my methods, performance, and to get out of my comfort zone to learn new skills and technologies.",
            "The most valuable is the complexity of knowledge I got during the last 5 years in different digital areas.",
          ]
        },
      ]
    }
  }
}
</script>
