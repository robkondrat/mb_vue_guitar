<template>
  <div>
    <div class="fretboard">
      <div class="fret" v-on:click="playNote()">
        E5
      </div>
      <div class="fret" v-on:click="playNote()">
        F5
      </div>
      <div class="fret" v-on:click="playNote()">
        F#5
      </div>
      <div class="fret" v-on:click="playNote()">
        G5
      </div>
      <div class="fret" v-on:click="playNote()">
        G#5
      </div>
      <div class="fret" v-on:click="playNote()">
        B4
      </div>
      <div class="fret" v-on:click="playNote()">
        C5
      </div>
      <div class="fret" v-on:click="playNote()">
        C#5
      </div>
      <div class="fret" v-on:click="playNote()">
        D5
      </div>
      <div class="fret" v-on:click="playNote()">
        D#5
      </div>
      <div class="fret" v-on:click="playNote()">
        G4
      </div>
      <div class="fret" v-on:click="playNote()">
        G#4
      </div>
      <div class="fret" v-on:click="playNote()">
        A4
      </div>
      <div class="fret" v-on:click="playNote()">
        A#4
      </div>
      <div class="fret" v-on:click="playNote()">
        B4
      </div>
      <div class="fret" v-on:click="playNote()">
        D4
      </div>
      <div class="fret" v-on:click="playNote()">
        D#4
      </div>
      <div class="fret" v-on:click="playNote()">
        E4
      </div>
      <div class="fret" v-on:click="playNote()">
        F4
      </div>
      <div class="fret" v-on:click="playNote()">
        F#4
      </div>
      <div class="fret" v-on:click="playNote()">
        A3
      </div>
      <div class="fret" v-on:click="playNote()">
        A#3
      </div>
      <div class="fret" v-on:click="playNote()">
        B3
      </div>
      <div class="fret" v-on:click="playNote()">
        C4
      </div>
      <div class="fret" v-on:click="playNote()">
        C#4
      </div>
      <div class="fret" v-on:click="playNote()">
        E3
      </div>
      <div class="fret" v-on:click="playNote()">
        F3
      </div>
      <div class="fret" v-on:click="playNote()">
        F#3
      </div>
      <div class="fret" v-on:click="playNote()">
        G3
      </div>
      <div class="fret" v-on:click="playNote()">
        G#3
      </div>
    </div>
  </div>
</template>

<script>

import { Synth } from 'tone'

export default {
  name: 'Fretboard',
  props: {
    msg: String
  },
  methods: {
    playNote() {
      const note = event.target.innerText
      console.log(note)
      this.synth = new Synth().toDestination();
      this.synth.triggerAttackRelease(note, "8n")
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
.fretboard {
  display: grid;
  grid-template-columns: auto auto auto auto auto;
  grid-column-gap: 50px;
  grid-row-gap: 50px;
}

</style>
