<template>
  <div class="hello">
    <h1>Cuatro en Raya</h1>
    <p>
      ¡Lucha contra la máquina!
    </p>
    
      <div class="main">
          <div class="container">
              <b-row class="row-y1">
                  <b-col class="col-y1">
                      <div class="circle" data-y="1" data-x="1"></div>
                  </b-col>
                  <b-col class="col-y1">
                      <div class="circle" data-y="1" data-x="2"></div>
                  </b-col>
                  <b-col class="col-y1">
                      <div class="circle" data-y="1" data-x="3"></div>
                  </b-col>
                  <b-col class="col-y1">
                      <div class="circle" data-y="1" data-x="4"></div>
                  </b-col>
              </b-row>
              <b-row class="row-y2">
                  <b-col class="col-y2">
                      <div class="circle" data-y="2" data-x="1"></div>
                  </b-col>
                  <b-col class="col-y2">
                      <div class="circle" data-y="2" data-x="2"></div>
                  </b-col>
                  <b-col class="col-y2">
                      <div class="circle" data-y="2" data-x="3"></div>
                  </b-col>
                  <b-col class="col-y2">
                      <div class="circle" data-y="2" data-x="4"></div>
                  </b-col>
              </b-row>
              <b-row class="row-y3">
                  <b-col class="col-y3">
                      <div class="circle" data-y="3" data-x="1"></div>
                  </b-col>
                  <b-col class="col-y3">
                      <div class="circle" data-y="3" data-x="2"></div>
                  </b-col>
                  <b-col class="col-y3">
                      <div class="circle" data-y="3" data-x="3"></div>
                  </b-col>
                  <b-col class="col-y3">
                      <div class="circle" data-y="3" data-x="4"></div>
                  </b-col>
              </b-row>
              <b-row class="row-y4">
                  <b-col class="col-y4">
                      <div class="circle" data-y="4" data-x="1"></div>
                  </b-col>
                  <b-col class="col-y4">
                      <div class="circle" data-y="4" data-x="2"></div>
                  </b-col>
                  <b-col class="col-y4">
                      <div class="circle" data-y="4" data-x="3"></div>
                  </b-col>
                  <b-col class="col-y4">
                      <div class="circle" data-y="4" data-x="4"></div>
                  </b-col>
              </b-row>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Game',
    data() {
        return {
            y1: ['', '', '', ''],
            y2: ['', '', '', ''],
            y3: ['', '', '', ''],
            y4: ['', '', '', ''],
        };
    },

    methods: {

    },

    created() {
        this.y1 = ['', '', '', ''];
        this.y2 = ['', '', '', ''];
        this.y3 = ['', '', '', ''];
        this.y4 = ['', '', '', ''];
        alert("Listo para empezar");
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    a {
      color: #42b983;
    }

    b-row{
        display: block;
    }

    .circle {
        height: 80px;
        width: 80px;
        border-radius: 100%;
        background-color: slategrey;
        display: inline-block;
        margin: 20px;
    }
</style>
