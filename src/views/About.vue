<template>
  <div>
    <select @change="updateOffWhite($event)" v-model="key" class="classic">
      <option value="init">CHOOOSE FILTER</option>
      <option value="offwhite">OFFWHITE</option>
    </select>
    <ul>
      <li v-for="(name,index,) in names" :key="index">
        <div class="card">
          <div class="card-content">
            <h1>{{name.name}}</h1>
            <p>
              <small>
                by
                <template v-if="name.brand=='Louis Vuitton'">
                  <a target="_blank">To be announced</a>
                </template>
                <template v-else>
                  <a target="_blank">{{name.brand}}</a>
                </template>
              </small>
            </p>
            <p class="related">
              <strong>Price:</strong>
              <a>{{name.price.price}} {{name.price.currency}}</a>
            </p>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

      <script>
import states from "../assets/products.json";
export default {
  name: "HelloWorld",
  data: () => ({
    brand: "Off-White",
    key: "",
    globalObject: []
  }),
  computed: {
    names() {
      this.globalObject = states.products;
      return this.globalObject;
    }
  },
  methods: {
    updateOffWhite() {
      if ((this.key = "offwhite")) {
        let filtered = this.globalObject.filter(
          name => (name.brand = "Off-White")
        );
        return (this.globalObject = filtered);
      }
    }
  }
};
</script>

      <!-- Add "scoped" attribute to limit CSS to this component only -->
      <style scoped lang="scss">
h1,
h2 {
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

.github-corner:hover .octo-arm {
  animation: octocat-wave 560ms ease-in-out;
}

@keyframes octocat-wave {
  0%,
  100% {
    transform: rotate(0);
  }

  20%,
  60% {
    transform: rotate(-25deg);
  }

  40%,
  80% {
    transform: rotate(10deg);
  }
}

@media (max-width: 500px) {
  .github-corner:hover .octo-arm {
    animation: none;
  }

  .github-corner .octo-arm {
    animation: octocat-wave 560ms ease-in-out;
  }
}

body {
  background: #edf2f4;
  perspective: 1000px;
  transform-style: preserve-3d;
  display: flex;
  height: 100vh;
  font-family: "Playfair Display", georgia, serif;
}
.card {
  pointer-events: none;
  transform: translateZ(0);
  padding: 30px;
  background: white;
  border-radius: 5px;
  width: 400px;
  height: 200px;
  margin: auto;
  transform-style: preserve-3d;
  backface-visibility: hidden;
  display: flex;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
  position: relative;

  &:after {
    content: " ";
    position: absolute;
    width: 100%;
    height: 10px;
    border-radius: 50%;
    left: 0;
    bottom: -50px;
    box-shadow: 0 30px 20px rgba(0, 0, 0, 0.3);
  }

  .card-content {
    margin: auto;
    text-align: center;
    transform-style: preserve-3d;
  }

  h1 {
    transform: translateZ(100px);
  }
  p {
    transform: translateZ(50px);
    display: block;

    &.related {
      transform: translateZ(80px);
      font-style: italic;
    }
  }
  a {
    color: #69c6b8;
    pointer-events: auto;
  }
}

select {
  /* styling */
  background-color: white;
  border: thin solid blue;
  border-radius: 4px;
  display: inline-block;
  font: inherit;
  line-height: 1.5em;
  padding: 0.5em 3.5em 0.5em 1em;

  /* reset */

  margin: 0;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  -webkit-appearance: none;
  -moz-appearance: none;
}

/* arrows */

select.classic {
  background-image: linear-gradient(45deg, transparent 50%, blue 50%),
    linear-gradient(135deg, blue 50%, transparent 50%),
    linear-gradient(to right, skyblue, skyblue);
  background-position: calc(100% - 20px) calc(1em + 2px),
    calc(100% - 15px) calc(1em + 2px), 100% 0;
  background-size: 5px 5px, 5px 5px, 2.5em 2.5em;
  background-repeat: no-repeat;
}

select.classic:focus {
  background-image: linear-gradient(45deg, white 50%, transparent 50%),
    linear-gradient(135deg, transparent 50%, white 50%),
    linear-gradient(to right, gray, gray);
  background-position: calc(100% - 15px) 1em, calc(100% - 20px) 1em, 100% 0;
  background-size: 5px 5px, 5px 5px, 2.5em 2.5em;
  background-repeat: no-repeat;
  border-color: grey;
  outline: 0;
}

select.round {
  background-image: linear-gradient(45deg, transparent 50%, gray 50%),
    linear-gradient(135deg, gray 50%, transparent 50%),
    radial-gradient(#ddd 70%, transparent 72%);
  background-position: calc(100% - 20px) calc(1em + 2px),
    calc(100% - 15px) calc(1em + 2px), calc(100% - 0.5em) 0.5em;
  background-size: 5px 5px, 5px 5px, 1.5em 1.5em;
  background-repeat: no-repeat;
}

select.round:focus {
  background-image: linear-gradient(45deg, white 50%, transparent 50%),
    linear-gradient(135deg, transparent 50%, white 50%),
    radial-gradient(gray 70%, transparent 72%);
  background-position: calc(100% - 15px) 1em, calc(100% - 20px) 1em,
    calc(100% - 0.5em) 0.5em;
  background-size: 5px 5px, 5px 5px, 1.5em 1.5em;
  background-repeat: no-repeat;
  border-color: green;
  outline: 0;
}

select.minimal {
  background-image: linear-gradient(45deg, transparent 50%, gray 50%),
    linear-gradient(135deg, gray 50%, transparent 50%),
    linear-gradient(to right, #ccc, #ccc);
  background-position: calc(100% - 20px) calc(1em + 2px),
    calc(100% - 15px) calc(1em + 2px), calc(100% - 2.5em) 0.5em;
  background-size: 5px 5px, 5px 5px, 1px 1.5em;
  background-repeat: no-repeat;
}

select.minimal:focus {
  background-image: linear-gradient(45deg, green 50%, transparent 50%),
    linear-gradient(135deg, transparent 50%, green 50%),
    linear-gradient(to right, #ccc, #ccc);
  background-position: calc(100% - 15px) 1em, calc(100% - 20px) 1em,
    calc(100% - 2.5em) 0.5em;
  background-size: 5px 5px, 5px 5px, 1px 1.5em;
  background-repeat: no-repeat;
  border-color: green;
  outline: 0;
}

select:-moz-focusring {
  color: transparent;
  text-shadow: 0 0 0 #000;
}

body {
  background-color: rgb(0, 159, 214);
  font: bold 1em/100% "Helvetica Neue", Arial, sans-serif;
  padding: 2em 0;
  text-align: center;
}
h1 {
  color: tomato;
  line-height: 120%;
  margin: 0 auto 2rem auto;
  max-width: 30rem;
}
</style>
