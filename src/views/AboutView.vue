<template>
  <div class="about">

    <h1 v-if="students.length == 1">Er is {{ students.length }} student</h1>
    <h1 v-else>Er zijn {{ students.length }} studenten</h1>

    <input type="text" v-model="newname" />
    <button :disabled="newname.length < 2 || students.length > 5" @click="addName();">toevoegen</button>
    <button @click="clearStudents();">leegmaken</button>

    <ul>
      <li v-for="name in students">{{ name }}</li>
    </ul>

  </div>
</template>

<script>

export default
{
  data() {
    return {
      students: ['Shannah', 'Laurens', 'Tim', 'Minka'],
      newname: ''
    }
  },

  methods: {
    addName()
    {
      this.students.push(this.newname);
    },

    clearStudents()
    {
      this.students = [];
    }
  }
}

</script>

<style>
</style>
