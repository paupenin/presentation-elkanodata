<template>
  <section v-bind:class="classObject" data-aos="fade-up" data-aos-delay="200">
    <div class="2">
        <h1 v-if="title" class="Slide__title">{{ title }}</h1>
        <h2 v-if="subtitle" class="Slide__subtitle">{{ subtitle }}</h2>
        <div v-if="content" class="Slide__content">
            <p v-for="(sentence, index) in content" :key="index">{{ sentence }}</p>
        </div>
    </div>
  </section>
</template>

<script>
export default {
  props: ['title', 'subtitle', 'content', 'small'],
  data() {
    return {
        'classObject': {
            'Slide': true,
            'Slide--is-small': !! this.small,
        }
    }
  }
}
</script>

<style>
.Slide {
  @apply flex items-center;

  min-height: 50vh;
}

.Slide--is-small {
 min-height: 10vh;
}

@screen md {
  .Slide__content {
    @apply ml-40;
  }
}
</style>
