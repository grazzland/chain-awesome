<template>
          <v-layout row wrap>
             <v-flex d-flex xs12 sm12 md12 v-for="(item,index) in navs" :key="index" :id="'nav_'+index" v-if="item.subs && item.subs.length>0">
                <card  :item="item"  />
             </v-flex>
              <v-spacer></v-spacer>
          </v-layout>
</template>

<script>
import card from '@/components/card'
export default {
  // data: () => ({
  // }),
  computed: {
    navs () {
      return this.$store.state.setting.navs
    }
  },
  components: {
    card
  }
}
</script>

<style>

</style>
