<template>
  <div class="layout-padding">
    <div>
      <q-icon :name="icon" class="gigi" style="font-size: 5rem;" @click="clicked" />
      <span style="margin: 0 15px;">{{icon}}</span>
      <q-icon :name="icon" class="gigi" style="font-size: 5rem;">
        <q-tooltip>{{icon}}</q-tooltip>
      </q-icon>
    </div>
    <q-option-group
      type="radio"
      v-model="icon"
      :options="[
        {value: 'cloud', label: 'A Material icon'},
        {value: 'mdi-airballoon', label: 'A MDI icon'},
        {value: 'fab fa-github', label: 'A Font Awesome icon'},
        {value: 'ion-airplane', label: 'A Ionicon (theme dependency)'},
        {value: 'ion-md-airplane', label: 'A Ionicon (md)'},
        {value: 'ion-ios-airplane', label: 'A Ionicon (ios)'}
      ]"
      style="margin-top: 25px"
    />
  </div>
</template>

<script>
export default {
  data () {
    return {
      icon: 'cloud'
    }
  },
  methods: {
    clicked () {
      console.log('clicked')
    }
  }
}
</script>
