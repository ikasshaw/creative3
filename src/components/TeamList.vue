<template>
  <div class="wrapper">
    <div class="teams">
      <div class="team" v-for="team in teams" :key="team.id">
        <div class="image">
          <img :src="'../images/team-logos/' + team.logo" />
        </div>
        <div class="info">
          <h2>{{ team.name }}</h2>
          <div class="drivers">
            <p>{{ driver_one(team.drivers[0]) }}</p>
            <p>{{ driver_two(team.drivers[1]) }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TeamList',
  props: {
    teams: Array,
    drivers: Array,
  },

  methods: {
    driver_one(index) {
      return this.$root.$data.drivers[index - 1].name;
    },
    driver_two(index) {
      return this.$root.$data.drivers[index - 1].name;
    },
  },
};
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.teams {
  /*margin-top: 20px;*/
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.team {
  display: flex;
  margin: 20px 10px 20px;
  height: 120px;
  width: 90vw;
  padding: 10px;
  border: 2px solid #333;
}

.image {
  display: flex;
  margin-right: 30px;
  height: 100px;
  width: 100px;
  justify-items: center;
  align-items: center;
}

.team img {
  max-height: 100px;
  max-width: 100px;
  object-fit: cover;
}

.info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  width: 100%;
  color: #000;
}

.info h2 {
  font-size: 1.5em;
  margin: 0;
  padding-bottom: 30px;
  align-self: center;
}

.drivers {
  display: flex;
  justify-content: space-around;
}

.info p {
  margin: 0px;
  font-size: 13px;
}

@media (min-width: 768px) {
  .team {
    width: 65vw;
  }
  .drivers {
    align-self: center;
    justify-self: center;
  }
  .drivers p {
    padding-right: 60px;
    padding-left: 60px;
    font-size: 1em;
  }
}

@media (min-width: 1200px) {
  .team {
    width: 50vw;
  }
}
</style>
