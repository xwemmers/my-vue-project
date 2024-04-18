<script>

export default {
  data() {
    return {
      name: 'Xander',
      age: 50
    }
  },

  methods: 
  {
    birthday() 
    {
      this.age++;
    },

    resetAge() 
    {
      this.age = 50;
    }
  }
}

</script>

<template>

  <h1>Mijn Vue applicatie</h1>

  <p>
    Mijn naam is {{ name }}
  </p>

  <p>
    Mijn leeftijd is {{ age }}
  </p>

  <button @click="birthday();">Jarig!</button>
  <button @click="resetAge();">Reset</button>

  <p>
    Mijn leeftijd is {{ age }}
  </p>

</template>
