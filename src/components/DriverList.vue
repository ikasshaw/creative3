<template>
  <div class="wrapper">
    <div class="drivers">
      <div class="driver" v-for="driver in drivers" :key="driver.id">
        <div class="name-country">
          <h2>{{ driver.name }}</h2>
          <p>{{ driver.country }}</p>
        </div>
        <div class="image">
          <img :src="'../../images/driver-pics/' + driver.image" />
        </div>
        <div class="info">
          <div class="team-number">
            <h2>{{ driver.team }}</h2>
            <h2>{{ driver.number }}</h2>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DriverList',

  props: {
    drivers: Array,
  },
};
</script>

<style scoped>
* {
  box-sizing: border-box;
}

.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.drivers {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  /*justify-content: center;*/
  width: 70vw;
}

.driver {
  display: flex;
  flex-direction: column;
  margin: 10px 10px 30px;
  height: 350px;
  border-bottom: 2px solid #d4d4d4;
}

.driver img {
  justify-self: center;
  max-height: 250px;
  max-width: 250px;
  object-fit: contain;
}

.driver .image {
  display: flex;
  margin-bottom: 5px;
  justify-self: center;
  background: black;
  height: 250px;
  width: 250px;
}

.info {
  display: flex;
  flex-direction: column;
  justify-self: center;
  align-self: center;
  justify-content: center;
  align-content: center;
  width: 100%;
}

.name-country {
  width: 100%;
  justify-content: space-between;
  align-content: start;
  margin: 0;
}

.name-country p,
h2 {
  margin: 0 3px 0 3px;
}

.team-number {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-content: start;
  margin: 0;
}

.team-number {
  margin: 0 3px 0 3px;
  font-size: 3em;
}

.team-number h2 {
  font-size: 20px;
}

.info p {
  margin: 0px;
  font-size: 10px;
}

@media (min-width: 768px) {
  .drivers {
    margin-top: 20px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-around;
  }

  .driver {
    margin: 50px 10px 10px;
    width: 250px;
  }
}
</style>
