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
                      <div class="circle" v-if="y1[0]==''" v-on:click="playerMove(1,1)"></div>
                      <div class="circleP" v-if="y1[0]=='0'"></div>
                      <div class="circleM" v-if="y1[0]=='1'"></div>
                  </b-col>
                  <b-col class="col-y1">
                      <div class="circle" v-if="y1[1]==''"  v-on:click="playerMove(1,2)"></div>
                      <div class="circleP" v-if="y1[1]=='0'"></div>
                      <div class="circleM" v-if="y1[1]=='1'"></div>
                  </b-col>
                  <b-col class="col-y1">
                      <div class="circle" v-if="y1[2]==''"  v-on:click="playerMove(1,3)"></div>
                      <div class="circleP" v-if="y1[2]=='0'"></div>
                      <div class="circleM" v-if="y1[2]=='1'"></div>
                  </b-col>
                  <b-col class="col-y1">
                      <div class="circle" v-if="y1[3]==''"  v-on:click="playerMove(1,4)"></div>
                      <div class="circleP" v-if="y1[3]=='0'"></div>
                      <div class="circleM" v-if="y1[3]=='1'"></div>
                  </b-col>
              </b-row>
              <b-row class="row-y2">
                  <b-col class="col-y2">
                      <div class="circle" v-if="y2[0]==''" v-on:click="playerMove(2,1)"></div>
                      <div class="circleP" v-if="y2[0]=='0'"></div>
                      <div class="circleM" v-if="y2[0]=='1'"></div>
                  </b-col>
                  <b-col class="col-y2">
                      <div class="circle" v-if="y2[1]==''" v-on:click="playerMove(2,2)"></div>
                      <div class="circleP" v-if="y2[1]=='0'"></div>
                      <div class="circleM" v-if="y2[1]=='1'"></div>
                  </b-col>
                  <b-col class="col-y2">
                      <div class="circle" v-if="y2[2]==''" v-on:click="playerMove(2,3)"></div>
                      <div class="circleP" v-if="y2[2]=='0'"></div>
                      <div class="circleM" v-if="y2[2]=='1'"></div>
                  </b-col>
                  <b-col class="col-y2">
                      <div class="circle" v-if="y2[3]==''" v-on:click="playerMove(2,4)"></div>
                      <div class="circleP" v-if="y2[3]=='0'"></div>
                      <div class="circleM" v-if="y2[3]=='1'"></div>
                  </b-col>
              </b-row>
              <b-row class="row-y3">
                  <b-col class="col-y3">
                      <div class="circle" v-if="y3[0]==''" v-on:click="playerMove(3,1)"></div>
                      <div class="circleP" v-if="y3[0]=='0'"></div>
                      <div class="circleM" v-if="y3[0]=='1'"></div>
                  </b-col>
                  <b-col class="col-y3">
                      <div class="circle" v-if="y3[1]==''" v-on:click="playerMove(3,2)"></div>
                      <div class="circleP" v-if="y3[1]=='0'"></div>
                      <div class="circleM" v-if="y3[1]=='1'"></div>
                  </b-col>
                  <b-col class="col-y3">
                      <div class="circle" v-if="y3[2]==''" v-on:click="playerMove(3,3)"></div>
                      <div class="circleP" v-if="y3[2]=='0'"></div>
                      <div class="circleM" v-if="y3[2]=='1'"></div>
                  </b-col>
                  <b-col class="col-y3">
                      <div class="circle" v-if="y3[3]==''" v-on:click="playerMove(3,4)"></div>
                      <div class="circleP" v-if="y3[3]=='0'"></div>
                      <div class="circleM" v-if="y3[3]=='1'"></div>
                  </b-col>
              </b-row>
              <b-row class="row-y4">
                  <b-col class="col-y4">
                      <div class="circle" v-if="y4[0]==''" v-on:click="playerMove(4,1)"></div>
                      <div class="circleP" v-if="y4[0]=='0'"></div>
                      <div class="circleM" v-if="y4[0]=='1'"></div>
                  </b-col>
                  <b-col class="col-y4">
                      <div class="circle" v-if="y4[1]==''" v-on:click="playerMove(4,2)"></div>
                      <div class="circleP" v-if="y4[1]=='0'"></div>
                      <div class="circleM" v-if="y4[1]=='1'"></div>
                  </b-col>
                  <b-col class="col-y4">
                      <div class="circle" v-if="y4[2]==''" v-on:click="playerMove(4,3)"></div>
                      <div class="circleP" v-if="y4[2]=='0'"></div>
                      <div class="circleM" v-if="y4[2]=='1'"></div>
                  </b-col>
                  <b-col class="col-y4">
                      <div class="circle" v-if="y4[3]==''" v-on:click="playerMove(4,4)"></div>
                      <div class="circleP" v-if="y4[3]=='0'"></div>
                      <div class="circleM" v-if="y4[3]=='1'"></div>
                  </b-col>
              </b-row>
              <b-row>
                  <b-col>
                      <b-button variant="danger" v-on:click="reset()">Reset</b-button>
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
            turn: 0,    //0: Jugador, 1: Máquina
            Mobjective: null    //Objetivo actual de la máquina
        };
    },

    methods: {
        playerMove(y, x) {

            if (this.turn == 0) {
                switch (y) {
                    case 1:
                        if (this.y1[x - 1] == '') {
                            this.y1[x - 1] = '0';

                            if (!this.checkVictory()) {
                                this.machineMove();
                            }
                            

                        } else {
                            console.log("Ya jugada");
                        }
                    break;

                    case 2:
                        if (this.y2[x - 1] == '') {
                            this.y2[x - 1] = '0';

                            if (!this.checkVictory()) {
                                this.machineMove();
                            }

                        } else {
                            console.log("Ya jugada");
                        }
                    break;

                    case 3:
                        if (this.y3[x - 1] == '') {
                            this.y3[x - 1] = '0';

                            if (!this.checkVictory()) {
                                this.machineMove();
                            }

                        } else {
                            console.log("Ya jugada");
                        }
                    break;

                    case 4:
                        if (this.y4[x - 1] == '') {
                            this.y4[x - 1] = '0';

                            if (!this.checkVictory()) {
                                this.machineMove();
                            }

                        } else {
                            console.log("Ya jugada");
                        }
                    break;
                }

            } else {
                console.log("¡Impaciente!");
            }
        },

        machineMove() {

        },

        checkVictory() {

            let victoryFlag = false;

            if (!this.y1.includes('')) {

                if (this.checkLine('y1')) {
                    victoryFlag = true;
                }

            } else if (!this.y2.includes('')) {

                if (this.checkLine('y2')) {
                    victoryFlag = true;
                }

            } else if (!this.y3.includes('')) {

                if (this.checkLine('y3')) {
                    victoryFlag = true;
                }

            } else if (!this.y4.includes('')) {

                if (this.checkLine('y4')) {
                    victoryFlag = true;
                }

            } else if (this.y1[0] != '' && this.y2[1] != '' && this.y3[2] != '' && this.y4[3] != '') {

                if (this.checkLine('d1')) {
                    victoryFlag = true;
                }

            } else if (this.y4[0] != '' && this.y3[1] != '' && this.y2[2] != '' && this.y1[3] != '') {

                if (this.checkLine('d2')) {
                    victoryFlag = true;
                }

            }
            
            if (victoryFlag) {
                alert("victoria");
                return true; //victoria
            } else {
                return false; //continua
            }
        },

        checkLine(line) {

            let allEqual = true;

            if (line == 'y1') {
                
                let searchVal = this.y1[0];

                for (var i1 = 0; i1 < this.y1; i1++) {
                    if (this.y1[i1] != searchVal) {
                        allEqual = false;
                    }
                }
            } else if (line == 'y2') {

                let searchVal = this.y1[0];

                for (var i2 = 0; i2 < this.y2; i2++) {
                    if (this.y2[i2] != searchVal) {
                        allEqual = false;
                    }
                }
            } else if (line == 'y3') {

                let searchVal = this.y1[0];

                for (var i3 = 0; i3 < this.y3; i3++) {
                    if (this.y3[i3] != searchVal) {
                        allEqual = false;
                    }
                }
            } else if (line == 'y4') {

                let searchVal = this.y1[0];

                for (var i4 = 0; i4 < this.y4; i4++) {
                    if (this.y4[i4] != searchVal) {
                        allEqual = false;
                    }
                }
            } else if (line == 'd1') {

                let searchVal = this.y1[0];

                if (this.y1[0] != searchVal || this.y2[1] != searchVal || this.y3[2] != searchVal || this.y4[3] != searchVal) {
                    allEqual = false;
                }
            } else if (line == 'd2') {

                let searchVal = this.y4[0];

                if (this.y4[0] != searchVal || this.y3[1] != searchVal || this.y2[2] != searchVal || this.y1[3] != searchVal) {
                    allEqual = false;
                }
            }

            if (allEqual) {
                return true
            }
        },

        reset() {
            this.y1 = ['', '', '', ''];
            this.y2 = ['', '', '', ''];
            this.y3 = ['', '', '', ''];
            this.y4 = ['', '', '', ''];
            this.turn = 0;
            this.Mobjective = null;
        }
    },

    created() {
        this.y1 = ['', '', '', ''];
        this.y2 = ['', '', '', ''];
        this.y3 = ['', '', '', ''];
        this.y4 = ['', '', '', ''];
        this.turn = 0;
        this.Mobjective = null;
        console.log("Listo para empezar a jugar");
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

    .circleP {
        height: 80px;
        width: 80px;
        border-radius: 100%;
        background-color: #aed65c;
        display: inline-block;
        margin: 20px;
    }

    .circleM {
        height: 80px;
        width: 80px;
        border-radius: 100%;
        background-color: #d96c68;
        display: inline-block;
        margin: 20px;
    }
</style>
