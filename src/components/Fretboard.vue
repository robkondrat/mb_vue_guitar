<template>
  <div>
    <div class="fretboard">
      <div class="fret">
        E
      </div>
      <div class="fret">
        F
      </div>
      <div class="fret">
        F#
      </div>
      <div class="fret">
        G
      </div>
      <div class="fret">
        G#
      </div>
      <div class="fret">
        B
      </div>
      <div class="fret">
        C
      </div>
      <div class="fret">
        C#
      </div>
      <div class="fret">
        D
      </div>
      <div class="fret">
        D#
      </div>
      <div class="fret">
        G
      </div>
      <div class="fret">
        G#
      </div>
      <div class="fret">
        A
      </div>
      <div class="fret">
        A#
      </div>
      <div class="fret">
        B
      </div>
      <div class="fret">
        D
      </div>
      <div class="fret">
        D#
      </div>
      <div class="fret">
        E
      </div>
      <div class="fret">
        F
      </div>
      <div class="fret">
        F#
      </div>
      <div class="fret">
        A
      </div>
      <div class="fret">
        A#
      </div>
      <div class="fret">
        B
      </div>
      <div class="fret">
        C
      </div>
      <div class="fret">
        C#
      </div>
      <div class="fret">
        E
      </div>
      <div class="fret">
        F
      </div>
      <div class="fret">
        F#
      </div>
      <div class="fret">
        G
      </div>
      <div class="fret" v-on:click="playC()">
        G#
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
    playC() {
      this.synth = new Synth().toDestination();
      this.synth.triggerAttackRelease("C4","8n")
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
