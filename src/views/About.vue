<template>
  <div class="about">
    <h2>current team: {{team.name}}</h2>
    <button @click="increase">counter</button>
    <p>{{ $store.state.sum }}</p>
    <p>Last team name clicked: {{team.name}}</p>
    <p>
      <router-link :to="{name: 'Home'}">戻る</router-link>
    </p>
  </div>
</template>

<script>
export default {
  props: ["team"],
  methods:{
    increase(){
      this.$store.dispatch("incrementAction");
    },
  },
  data() {
    return {
      teams: [
        {
          id: "c36136ef-552f-4dc9-84b6-65ecb8574e81",
          name: "Team_A",
        },
        {
          id: "ed0459f5-716d-4ef4-99ba-5dc750dfe0d0",
          name: "Team_B",
        },
        {
          id: "60d0d5d5-8ce9-41d9-a65b-13a090c10ae1",
          name: "Team_C",
        },
      ]
    };
  }
};
</script>