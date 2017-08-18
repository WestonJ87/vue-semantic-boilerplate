<template>
  <!-- IMPORTANT :  It is important that the parent DIV is not the div that needs activating for Semantic.js -->
  <div id="semantic-playground-body">

    <!-- Accordion -->
    <div class="ui styled fluid accordion">
    <div class="title">
      <i class="dropdown icon"></i>
      What is a dog?
    </div>
    <div class="content">
      <p class="transition hidden">{{ msg }} <br>A dog is a type of domesticated animal. Known for its loyalty and faithfulness, it can be found as a welcome guest in many households across the world.</p>
    </div>
    <div class="title active">
      <i class="dropdown icon"></i>
      What kinds of dogs are there?
    </div>
    <div class="content active">
      <p class="transition visible">There are many breeds of dogs. Each breed varies in size and temperament. Owners often select a breed of dog that they find to be compatible with their own lifestyle and desires from a companion.</p>
    </div>
    <div class="title">
      <i class="dropdown icon"></i>
      How do you acquire a dog?
    </div>
    <div class="content">
      <p>Three common ways for a prospective owner to acquire a dog is from pet shops, private owners, or shelters.</p>
      <p>A pet shop may be the most convenient way to buy a dog. Buying a dog from a private owner allows you to assess the pedigree and upbringing of your dog before choosing to take it home. Lastly, finding your dog from a shelter, helps give a good home to a dog who may not find one so readily.</p>
    </div>
  </div>

  <div id="cards">
    <!-- Cards -->
    <div class="ui link centered cards">
    <div class="card">
      <div class="image">
        <img src="https://api.adorable.io/avatars/285/leroy@adorable.io.png">
      </div>
      <div class="content">
        <div class="header">Matt Giampietro</div>
        <div class="meta">
          <a>Friends</a>
        </div>
        <div class="description">
          Matthew is an interior designer living in New York.
        </div>
      </div>
      <div class="extra content">
        <span class="right floated">
          Joined in 2013
        </span>
        <span>
          <i class="user icon"></i>
          75 Friends
        </span>
      </div>
    </div>
    <div class="card">
      <div class="image">
        <img src="https://api.adorable.io/avatars/285/molly@adorable.io.png">
      </div>
      <div class="content">
        <div class="header">Molly</div>
        <div class="meta">
          <span class="date">Coworker</span>
        </div>
        <div class="description">
          Molly is a personal assistant living in Paris.
        </div>
      </div>
      <div class="extra content">
        <span class="right floated">
          Joined in 2011
        </span>
        <span>
          <i class="user icon"></i>
          35 Friends
        </span>
      </div>
    </div>
    <div class="card">
      <div class="image">
        <img src="https://api.adorable.io/avatars/285/elyse@adorable.io.png">
      </div>
      <div class="content">
        <div class="header">Elyse</div>
        <div class="meta">
          <a>Coworker</a>
        </div>
        <div class="description">
          Elyse is a copywriter working in New York.
        </div>
      </div>
      <div class="extra content">
        <span class="right floated">
          Joined in 2014
        </span>
        <span>
          <i class="user icon"></i>
          151 Friends
        </span>
      </div>
    </div>
  </div>
  </div>

  <router-link to="/" class="back-home-link"> Back to Home </router-link>
</div>
</template>

<script>
export default {
  name: 'semantic',
  data () {
    return {
      msg: 'This is not the message you were looking for!'
    }
  },
  mounted: function () {
    console.log("MOUNTED");
    this.initializeSemantic();
  },
  ready: function () {
    console.log("READY");
    this.initializeSemantic();
  },
  methods: {
    initializeSemantic: function () {
      console.log($(this.$el));
      console.log("INITIALIZING ui.accordions :: ", $(this.$el).find('.ui.accordion') );
      // Update elements to match what is needed by Semantic.js
      $(this.$el).find('.ui.accordion').accordion();
    }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  a {
    color: #42b983;
  }

  #cards {
    margin-top: 60px;
  }

  .back-home-link {
    margin-top: 60px;
  }
</style>
