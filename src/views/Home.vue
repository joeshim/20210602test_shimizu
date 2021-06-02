<template>
  <div class="home">
    <h2>チーム一覧</h2>
    <div v-for="team in teams" :key="team.id">
      <router-link :to="{name: 'About', params: {team}}">{{ team.name }}</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  props:["team"],
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
      ],
    };
  }
};
</script>

<style scoped>
div {
  line-height: 30px;
}
</style>