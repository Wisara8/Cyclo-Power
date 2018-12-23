<template>
  <main class="container">
    <nav>
      <div class="toggle_button">
        <i class="fas fa-grip-lines fa-2x"></i>
      </div>
      <div class="nav_top_header">
        <img src="https://api.adorable.io/avatars/285/abott@adorable.png" alt="user_icon" class="user_icon">
      </div>
      <div class="nav_items">
        <h1 class="user_name">
          User Name
        </h1>

        <p class="user_text"> I am a placeholderI am a placeholderI am a placeholderI am a placeholderI am a placeholder </p>

        <ul class="nav_list">
          <li class="nav_item" v-on:click="activity"> My Activity</li>
          <li class="nav_item" v-on:click="trophy"> My Trophies </li>
          <li class="nav_item" v-on:click="lottery"> Lottery </li>
          <li class="nav_item" v-on:click="statistics"> My Statistics </li>
        </ul>
      </div>
    </nav>

    <content class="main_content">
      <component v-bind:is="component"></component>
    </content>
  </main>
</template>

<script>
  import UserActivity from './UserActivity.vue';
  import Trophy from './Trophy.vue';
  import Lottery from './Lottery.vue';
  import Stats from './Stats.vue';

  export default {
    components: {
      'user_activity': UserActivity,
      'trophies': Trophy,
      'lottery': Lottery,
      'stats': Stats,
    },
    data() {
      return {
        component: 'user_activity'
      }
    },
    methods: {
      activity: function(event) {
        this.component = 'user_activity';
      },
      trophy: function(event) {
        this.component = 'trophies';
      },
      lottery: function(event) {
        this.component = 'lottery';
      },
      statistics: function(event) {
        this.component = 'stats';
      }
    }
  }
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>

</style>
