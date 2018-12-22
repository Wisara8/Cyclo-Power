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
          <li class="nav_item" v-on:click="activity"> Item 1 </li>
          <li class="nav_item" v-on:click="second"> Item 2 </li>
          <li class="nav_item"> Item 3 </li>
          <li class="nav_item"> Item 4 </li>
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
  import Placeholder from './Placeholder.vue';

  export default {
    components: {
      'user_activity': UserActivity,
      'placeholder': Placeholder
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
      second: function(event) {
        this.component = 'placeholder';
      }
    }
  }
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>

</style>
