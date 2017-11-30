<template>
  <div class="hello">
    <div class="ui labeled button" tabindex="0">
      <div class="ui red button">
        <i class="heart icon"></i> Like
      </div>
      <a class="ui basic red left pointing label">
        1,048
      </a>
    </div>

    <div :class="['ui', {'active': isShowModal}, 'modal']">
      <div class="ui icon header">
        <i class="archive icon"></i>
        Archive Old Messages
      </div>
      <div class="content">
        <p>Your inbox is getting full, would you like us to enable automatic archiving of old messages?</p>
      </div>
      <div class="actions">
        <div class="ui red cancel inverted button">
          <i class="remove icon"></i>
          No
        </div>
        <div class="ui green ok inverted button">
          <i class="checkmark icon"></i>
          Yes
        </div>
      </div>
    </div>

    <button class="ui green button" @click.prevent="showModal">Show modal</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      isShowModal: false
    }
  },

  methods: {
    showModal () {
      $('.ui.modal')
        .modal('show')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
