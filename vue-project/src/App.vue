<script setup>
  import HelloWorld from './components/HelloWorld.vue'

</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/author.png" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
      <div class="wrapper">
        <!-- print -->
        <h2 class="font-bold text-red-500">{{ msg }}</h2>
        
        <!-- loop -->
        <div v-for="course in courses" class="font-bold text-red-500">
          <div class="shadow p-4 mb-4 border border-gray-20">
            <h1>{{ course.id }}.{{ course.name }}</h1>
            <p>{{ course.des }}</p>
          </div>  
        </div>
      </div>
  </main>
</template>
<script>
  export default{
    name :'App',
    data(){
      return{
        msg:'Welcome Vue js App',
        courses : [
          {
            id:1,
            name: 'Vue JS',
            des: 'The Progressive JavaScript Framework',
          },
          {
            id:2,
            name: 'Nuxt JS',
            des: 'The Progressive Vue JS Framework',
          },
        ],
      }
      
    }
  }
</script>
<style scoped>
  header {
    line-height: 1.5;
  }

  .logo {
    display: block;
    margin: 0 auto 2rem;
  }

  @media (min-width: 1024px) {
    header {
      display: flex;
      place-items: center;
      padding-right: calc(var(--section-gap) / 2);
    }

    .logo {
      margin: 0 2rem 0 0;
    }

    header .wrapper {
      display: flex;
      place-items: flex-start;
      flex-wrap: wrap;
    }
  }
</style>
