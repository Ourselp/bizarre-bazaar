<template>
  <div class="c-navbar">
    <div class="c-navbar-left">
      <div class="c-navbar-left-box">
        <span class="c-navbar-left-box-icon">
          <img src="@/assets/TopNavbar/icon.png"/>
        </span>
      </div>
      <div class="c-navbar-left-box">
        About Me
      </div>
    </div>

    <div class="c-navbar-right">
      <div class="c-navbar-right-box">
        <span class="c-navbar-right-box-time">
          {{ hours }}:{{ minutes }}:{{ seconds }}
        </span>
      </div>
      <div class="c-navbar-right-box">
        {{ date.toLocaleDateString("en-US", this.options) }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TopNavbar',

  data() {
    return {
      date: new Date(),
      options: { weekday: 'long', month: 'long', day: 'numeric' },
      hours: 0,
      minutes: 0,
      seconds: 0,
    }
  },

  methods: {
    setTime() {
      const date = new Date();
      let hours = date.getHours();
      let minutes = date.getMinutes();
      let seconds = date.getSeconds();
      hours = hours <= 9 ? `${hours}`.padStart(2, 0) : hours;
      minutes = minutes <= 9 ? `${minutes}`.padStart(2, 0) : minutes;
      seconds = seconds <= 9 ? `${seconds}`.padStart(2, 0) : seconds;
      this.hours = hours;
      this.minutes = minutes;
      this.seconds = seconds;
    }
  },

  mounted() {
    setInterval(() => this.setTime(), 1000)
  },
}
</script>
