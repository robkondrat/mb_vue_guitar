<template>
  <div>
    <div class="fretboard">
      <div class="fret" v-on:click="playNote()" v-for="note in notes" :key="note.message">{{ note.message }}</div>
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
  data() {
    return {
      notes: [
      { message: "E5" },
      { message: "F5" },
      { message: "F#5" },
      { message: "G5" },
      { message: "G#5" },
      { message: "B4" },
      { message: "C5" },
      { message: "C#5" },
      { message: "D5" },
      { message: "D#5" },
      { message: "G4" },
      { message: "G#4" },
      { message: "A4" },
      { message: "A#4" },
      { message: "b4" },
      { message: "D4" },
      { message: "D#4" },
      { message: "E4" },
      { message: "F4" },
      { message: "F#4" },
      { message: "A3" },
      { message: "A#3" },
      { message: "B3" },
      { message: "C4" }, 
      { message: "C#4" }, 
      { message: "E3" },
      { message: "F3" },
      { message: "F#3" },
      { message: "G3" },
      { message: "G#3" }
    ]
    };
  },
  methods: {
    playNote() {
      const note = event.target.innerText
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
  grid-template-rows: auto;
  grid-column-gap: none;
  grid-row-gap: 5px;
  font-size: auto;
  border: 2px solid black;
  cursor: url(https://www.pinclipart.com/picdir/middle/83-837567_png-file-finger-pointing-down-transparent-clipart.png), auto;
}
.fret {
  background-color: brown;
}
.fret:nth-last-child(5n) {
  background-color: grey;
  border-right: 2px solid black;
}


</style>
