<template>
  <div class="hello">
    <h1>Cuatro en Raya</h1>
    <p>
      {{msg}}
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
            mObjective: null,    //Objetivo actual de la máquina
            msg: "¡Lucha contra la máquina!",
            victory: false
        };
    },

    methods: {
        playerMove(y, x) { //Jugador Hace click en casilla

            if (this.turn == 0 && !this.victory) {
                switch (y) {
                    case 1:
                        if (this.y1[x - 1] == '') {
                            this.y1[x - 1] = '0';

                            if (!this.checkVictory()) {
                                this.turn = 1; //turno de la máquina
                                this.machineMove();
                            }
                            

                        } else {
                            this.msg = "Ya jugada";
                        }
                    break;

                    case 2:
                        if (this.y2[x - 1] == '') {
                            this.y2[x - 1] = '0';

                            if (!this.checkVictory()) {
                                this.turn = 1; //turno de la máquina
                                this.machineMove();
                            }

                        } else {
                            this.msg = "Ya jugada";
                        }
                    break;

                    case 3:
                        if (this.y3[x - 1] == '') {
                            this.y3[x - 1] = '0';

                            if (!this.checkVictory()) {
                                this.turn = 1; //turno de la máquina
                                this.machineMove();
                            }

                        } else {
                            this.msg = "Ya jugada";
                        }
                    break;

                    case 4:
                        if (this.y4[x - 1] == '') {
                            this.y4[x - 1] = '0';

                            if (!this.checkVictory()) {
                                this.turn = 1; //turno de la máquina
                                this.machineMove();
                            }

                        } else {
                            this.msg = "Ya jugada";
                        }
                    break;
                }

            } else {
                this.msg = "¡Impaciente!";
            }
        },

        machineMove() {//Movimiento de máquina
            if (this.mObjective == null) {//Buscar un objetivo
                this.machineSearch();
            }

            var ObjViable = true; //Objetivo viable

            if (this.mObjective != false) {//Si la máquina aún tiene posibilidades
                
                switch (this.mObjective) {
                    case 'y1':
                        for (let indY1 = 0; indY1 < this.y1.length; indY1++) {//Comprobar si sigue siendo viable
                            if (this.y1[indY1] == '0') {
                                ObjViable = false;
                                this.mObjective = null;
                                this.machineMove();
                                return false;
                            }
                        }

                        if (ObjViable) {//la línea es viable
                            for (let indY1 = 0; indY1 < this.y1.length; indY1++) {
                                if (this.y1[indY1] == '') {
                                    this.y1[indY1] = '1';//Marcar siguiente casilla
                                    break;
                                }
                            }
                        } else {//la línea ya no es viable
                            this.machineMove()
                            return false;
                        }
                    break;

                    case 'y2':
                        for (let indY2 = 0; indY2 < this.y2.length; indY2++) {//Comprobar si sigue siendo viable
                            if (this.y2[indY2] == '0') {
                                ObjViable = false;
                                this.mObjective = null;
                                this.machineMove();
                                return false;
                            }
                        }

                        if (ObjViable) {//la línea es viable
                            for (let indY2 = 0; indY2 < this.y2.length; indY2++) {
                                if (this.y2[indY2] == '') {
                                    this.y2[indY2] = '1';//Marcar siguiente casilla
                                    break;
                                }
                            }
                        } else {//la línea ya no es viable
                            this.machineMove()
                            return false;
                        }
                    break;

                    case 'y3':
                        for (let indY3 = 0; indY3 < this.y3.length; indY3++) {//Comprobar si sigue siendo viable
                            if (this.y3[indY3] == '0') {
                                ObjViable = false;
                                this.mObjective = null;
                                this.machineMove();
                                return false;
                            }
                        }

                        if (ObjViable) {//la línea es viable
                            for (let indY3 = 0; indY3 < this.y3.length; indY3++) {
                                if (this.y3[indY3] == '') {
                                    this.y3[indY3] = '1';//Marcar siguiente casilla
                                    break;
                                }
                            }
                        } else {//la línea ya no es viable
                            this.machineMove()
                            return false;
                        }
                    break;

                    case 'y4':
                        for (let indY4 = 0; indY4 < this.y4.length; indY4++) {//Comprobar si sigue siendo viable
                            if (this.y4[indY4] == '0') {
                                ObjViable = false;
                                this.mObjective = null;
                                this.machineMove();
                                return false;
                            }
                        }

                        if (ObjViable) {//la línea es viable
                            for (let indY4 = 0; indY4 < this.y4.length; indY4++) {
                                if (this.y4[indY4] == '') {
                                    this.y4[indY4] = '1';//Marcar siguiente casilla
                                    break;
                                }
                            }
                        } else {//la línea ya no es viable
                            this.machineMove()
                            return false;
                        }
                    break;

                    case 'd1':
                        //Comprobar si sigue siendo viable
                        if (this.y1[0] == '0' || this.y2[1] == '0' || this.y3[2] == '0' || this.y4[3] == '0') {
                            ObjViable = false;
                            this.mObjective = null;
                            this.machineMove();
                            return false;
                        }

                        if (ObjViable) {//la línea es viable

                            //Marcar siguiente casilla
                            if (this.y1[0] == '') {
                                this.y1[0] = '1';

                            } else if (this.y2[1] == '') {
                                this.y2[1] = '1';

                            } else if (this.y3[2] == '') {
                                this.y3[2] = '1';

                            } else if (this.y4[3] == '') {
                                this.y4[3] = '1';
                            }

                        } else {//la línea ya no es viable
                            this.machineMove()
                            return false;
                        }
                    break;

                    case 'd2':
                        //Comprobar si sigue siendo viable
                        if (this.y4[0] == '0' || this.y3[1] == '0' || this.y2[2] == '0' || this.y1[3] == '0') {
                            ObjViable = false;
                            this.mObjective = null;
                            this.machineMove();
                            return false;
                        }

                        if (ObjViable) {//la línea es viable

                            //Marcar siguiente casilla
                            if (this.y4[0] == '') {
                                this.y4[0] = '1';

                            } else if (this.y3[1] == '') {
                                this.y3[1] = '1';

                            } else if (this.y2[2] == '') {
                                this.y2[2] = '1';

                            } else if (this.y1[3] == '') {
                                this.y1[3] = '1';
                            }

                        } else {//la línea ya no es viable
                            this.machineMove()
                            return false;
                        }
                    break;

                    case 'x1':
                        //Comprobar si sigue siendo viable
                        if (this.y1[0] == '0' || this.y2[0] == '0' || this.y3[0] == '0' || this.y4[0] == '0') {
                            ObjViable = false;
                            this.mObjective = null;
                            this.machineMove();
                            return false;
                        }

                        if (ObjViable) {//la línea es viable

                            //Marcar siguiente casilla
                            if (this.y1[0] == '') {
                                this.y1[0] = '1';

                            } else if (this.y2[0] == '') {
                                this.y2[0] = '1';

                            } else if (this.y3[0] == '') {
                                this.y3[0] = '1';

                            } else if (this.y4[0] == '') {
                                this.y4[0] = '1';
                            }

                        } else {//la línea ya no es viable
                            this.machineMove()
                            return false;
                        }
                    break;

                    case 'x2':
                        //Comprobar si sigue siendo viable
                        if (this.y1[1] == '0' || this.y2[1] == '0' || this.y3[1] == '0' || this.y4[1] == '0') {
                            ObjViable = false;
                            this.mObjective = null;
                            this.machineMove();
                            return false;
                        }

                        if (ObjViable) {//la línea es viable

                            //Marcar siguiente casilla
                            if (this.y1[1] == '') {
                                this.y1[1] = '1';

                            } else if (this.y2[1] == '') {
                                this.y2[1] = '1';

                            } else if (this.y3[1] == '') {
                                this.y3[1] = '1';

                            } else if (this.y4[1] == '') {
                                this.y4[1] = '1';
                            }

                        } else {//la línea ya no es viable
                            this.machineMove()
                            return false;
                        }
                    break;

                    case 'x3':
                        //Comprobar si sigue siendo viable
                        if (this.y1[2] == '0' || this.y2[2] == '0' || this.y3[2] == '0' || this.y4[2] == '0') {
                            ObjViable = false;
                            this.mObjective = null;
                            this.machineMove();
                            return false;
                        }

                        if (ObjViable) {//la línea es viable

                            //Marcar siguiente casilla
                            if (this.y1[2] == '') {
                                this.y1[2] = '1';

                            } else if (this.y2[2] == '') {
                                this.y2[2] = '1';

                            } else if (this.y3[2] == '') {
                                this.y3[2] = '1';

                            } else if (this.y4[2] == '') {
                                this.y4[2] = '1';
                            }

                        } else {//la línea ya no es viable
                            this.machineMove()
                            return false;
                        }
                    break;

                    case 'x4':
                        //Comprobar si sigue siendo viable
                        if (this.y1[3] == '0' || this.y2[3] == '0' || this.y3[3] == '0' || this.y4[3] == '0') {
                            ObjViable = false;
                            this.mObjective = null;
                            this.machineMove();
                            return false;
                        }

                        if (ObjViable) {//la línea es viable

                            //Marcar siguiente casilla
                            if (this.y1[3] == '') {
                                this.y1[3] = '1';

                            } else if (this.y2[3] == '') {
                                this.y2[3] = '1';

                            } else if (this.y3[3] == '') {
                                this.y3[3] = '1';

                            } else if (this.y4[3] == '') {
                                this.y4[3] = '1';
                            }

                        } else {//la línea ya no es viable
                            this.machineMove()
                            return false;
                        }
                    break;
                }

            } else {//Si la máquina está sin posibilidades
                this.msg = "¡Oye!";
            }

            if (!this.checkVictory()) {
                this.turn = 0;
            }
        },

        machineSearch() {//Máquina busca objetivo para completar
            var posibilities = ['y1', 'y2', 'y3', 'y4', 'd1', 'd2', 'x1', 'x2', 'x3', 'x4'];//Posibilidades para línea

            //Eliminar líneas ocupadas
            //Y1
            for (var indY1 = 0; indY1 < this.y1.length; indY1++) {
                if (this.y1[indY1] == '0') {
                    const index = posibilities.indexOf('y1');

                    if (index > -1) {
                        posibilities.splice(index, 1);
                    }

                    break;
                }
            }
            //Y2
            for (var indY2 = 0; indY2 < this.y2.length; indY2++) {
                if (this.y2[indY2] == '0') {
                    const index = posibilities.indexOf('y2');

                    if (index > -1) {
                        posibilities.splice(index, 1);
                    }

                    break;
                }
            }
            //Y3
            for (var indY3 = 0; indY3 < this.y3.length; indY3++) {
                if (this.y3[indY3] == '0') {
                    const index = posibilities.indexOf('y3');

                    if (index > -1) {
                        posibilities.splice(index, 1);
                    }

                    break;
                }
            }
            //Y4
            for (var indY4 = 0; indY4 < this.y4.length; indY4++) {
                if (this.y4[indY4] == '0') {
                    const index = posibilities.indexOf('y4');

                    if (index > -1) {
                        posibilities.splice(index, 1);
                    }

                    break;
                }
            }

            //D1
            if (this.y1[0] == '0' || this.y2[1] == '0' || this.y3[2] == '0' || this.y4[3] == '0') {
                const index = posibilities.indexOf('d1');

                if (index > -1) {
                    posibilities.splice(index, 1);
                }
            }

            //D2
            if (this.y4[0] == '0' || this.y3[1] == '0' || this.y2[2] == '0' || this.y1[3] == '0') {
                const index = posibilities.indexOf('d2');

                if (index > -1) {
                    posibilities.splice(index, 1);
                }
            }

            //X1
            if (this.y1[0] == '0' || this.y2[0] == '0' || this.y3[0] == '0' || this.y4[0] == '0') {
                const index = posibilities.indexOf('x1');

                if (index > -1) {
                    posibilities.splice(index, 1);
                }
            }

            //X2
            if (this.y1[1] == '0' || this.y2[1] == '0' || this.y3[1] == '0' || this.y4[1] == '0') {
                const index = posibilities.indexOf('x2');

                if (index > -1) {
                    posibilities.splice(index, 1);
                }
            }

            //X3
            if (this.y1[2] == '0' || this.y2[2] == '0' || this.y3[2] == '0' || this.y4[2] == '0') {
                const index = posibilities.indexOf('x3');

                if (index > -1) {
                    posibilities.splice(index, 1);
                }
            }

            //X4
            if (this.y1[3] == '0' || this.y2[3] == '0' || this.y3[3] == '0' || this.y4[3] == '0') {
                const index = posibilities.indexOf('x4');

                if (index > -1) {
                    posibilities.splice(index, 1);
                }
            }
            if (posibilities.length != 0) {
                this.mObjective = posibilities[Math.floor(Math.random() * posibilities.length)];
            } else {
                this.mObjective = false;
            }

        },

        checkVictory() { //Comprobar si hay victoria

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

            } else if (this.y1[0] != '' && this.y2[0] != '' && this.y3[0] != '' && this.y4[0] != '') {

                if (this.checkLine('x1')) {
                    victoryFlag = true;
                }

            } else if (this.y1[1] != '' && this.y2[1] != '' && this.y3[1] != '' && this.y4[1] != '') {

                if (this.checkLine('x2')) {
                    victoryFlag = true;
                }

            } else if (this.y1[2] != '' && this.y2[2] != '' && this.y3[2] != '' && this.y4[2] != '') {

                if (this.checkLine('x3')) {
                    victoryFlag = true;
                }

            } else if (this.y1[3] != '' && this.y2[3] != '' && this.y3[3] != '' && this.y4[3] != '') {

                if (this.checkLine('x4')) {
                    victoryFlag = true;
                }

            }
            
            if (victoryFlag) {
                this.victory = true;

                if (this.turn == 0) {
                    this.msg = "¡Victoria del jugador! >:(";
                } else {
                    this.msg = "¡La máquina gana! ;)"
                }
                return true; //victoria
            } else {
                return false; //continua
            }
        },

        checkLine(line) { //Comprobar si lineas tienen todas el mismo valor

            let allEqual = true;

            if (line == 'y1') {
                
                let searchVal = this.y1[0];

                for (var i1 = 0; i1 < this.y1; i1++) {
                    if (this.y1[i1] != searchVal) {
                        allEqual = false;
                    }
                }
            } else if (line == 'y2') {

                let searchVal = this.y2[0];

                for (var i2 = 0; i2 < this.y2; i2++) {
                    if (this.y2[i2] != searchVal) {
                        allEqual = false;
                    }
                }
            } else if (line == 'y3') {

                let searchVal = this.y3[0];

                for (var i3 = 0; i3 < this.y3; i3++) {
                    if (this.y3[i3] != searchVal) {
                        allEqual = false;
                    }
                }
            } else if (line == 'y4') {

                let searchVal = this.y4[0];

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
            } else if (line == 'x1') {

                let searchVal = this.y1[0];

                if (this.y1[0] != searchVal || this.y2[0] != searchVal || this.y3[0] != searchVal || this.y4[0] != searchVal) {
                    allEqual = false;
                }
            } else if (line == 'x2') {

                let searchVal = this.y1[1];

                if (this.y1[1] != searchVal || this.y2[1] != searchVal || this.y3[1] != searchVal || this.y4[1] != searchVal) {
                    allEqual = false;
                }
            } else if (line == 'x3') {

                let searchVal = this.y1[2];

                if (this.y1[2] != searchVal || this.y2[2] != searchVal || this.y3[2] != searchVal || this.y4[2] != searchVal) {
                    allEqual = false;
                }
            } else if (line == 'x4') {

                let searchVal = this.y1[3];

                if (this.y1[3] != searchVal || this.y2[3] != searchVal || this.y3[3] != searchVal || this.y4[3] != searchVal) {
                    allEqual = false;
                }
            }

            if (allEqual) {
                return true;
            } else {
                return false;
            }
        },

        reset() {
            this.y1 = ['', '', '', ''];
            this.y2 = ['', '', '', ''];
            this.y3 = ['', '', '', ''];
            this.y4 = ['', '', '', ''];
            this.turn = 0;
            this.mObjective = null;
            this.victory = false;
            this.msg = "¡Lucha contra la máquina!";
        }
    },

    created() {
        this.y1 = ['', '', '', ''];
        this.y2 = ['', '', '', ''];
        this.y3 = ['', '', '', ''];
        this.y4 = ['', '', '', ''];
        this.turn = 0;
        this.mObjective = null;
        this.victory = false;
        this.msg = "¡Lucha contra la máquina!";
        console.log("Listo para empezar a jugar");
    },
}
</script>

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
