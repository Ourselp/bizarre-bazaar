<template>
  <div class="c-jsheeps">
    <div class="animal">

      <div class="sheep">
        <div class="sheep-head">
          <div class="sheep-head-wool" />
          <div class="sheep-head-wool" />
          <div class="sheep-head-wool" />

          <div class="sheep-head-ears">
            <div class="sheep-head-ears-ear"/>
            <div class="sheep-head-ears-ear" />
          </div>

          <div class="sheep-head-eyes">
            <div class="sheep-head-eyes-eye">
              <div class="sheep-head-eyes-eye-pupil">
              </div>
            </div>

            <div class="sheep-head-eyes-eye">
              <div class="sheep-head-eyes-eye-pupil">
              </div>
            </div>
          </div>
        </div>

        <div class="sheep-body">
          <div class="sheep-body-wool" v-for="(wool, index) in wools" :key="wool">
            <div :class="'sheep-body-wool-hair sheep-body-wool-hair-' + index" />
          </div>
        </div>

        <div class="sheep-legs">
          <div :class="'sheep-legs-leg sheep-legs-leg-' + index" v-for="(leg, index) in legs" :key="leg"/>
        </div>

        <div class="sheep-tail">
          <div :class="'sheep-tail-wool sheep-tail-wool-' + index" v-for="(wool, index) in tails" :key="wool">
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'JumpingSheeps',

  data() {
      return {
          wools: [...Array(12)],
          legs: [...Array(4)],
          tails: [...Array(6)]
      }
  },
}
</script>
