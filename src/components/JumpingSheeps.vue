<template>
  <div class="c-jsheeps">

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

        <div class="sheep-body-legs">
          
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
          wools: [...Array(12)]
      }
  },
}
</script>
