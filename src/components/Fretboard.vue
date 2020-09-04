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
      console.log(note);
      this.synth = new Synth().toDestination();
      this.synth.triggerAttackRelease(note, "8n")
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body {
}
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
  grid-row-gap: none;
  font-size: auto;
  color: white;
  border: 2px solid black;

  cursor: url('../assets/hand2.png') 20 50, auto;

  background-image: url('https://media.istockphoto.com/photos/natural-wood-texture-picture-id1145602814?k=6&m=1145602814&s=612x612&w=0&h=2uVxc6l0CPalA8JV8XqpMcVVLrP9r-zr5jttpByEX-0=');
  background-repeat: no-repeat;
  background-size: cover;
}
.fret {
  border-bottom: 1px solid black;
  border-right: 2px solid white;
}
.fret:nth-last-child(5n) {
  background-color: grey;
  border-right: 2px solid black;
}


</style>
