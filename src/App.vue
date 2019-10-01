<template>
  <div id="app">
    <button type="button" @click="append">要素を追加</button>
    <div class="flex">
      <ul>
        <li v-for="(x, i) in items" :key="i">
          <span>{{ x }},{{ gen(i) }}</span>
        </li>
      </ul>
      <ul>
        <li v-for="(x, i) in items" :key="i">
          <list-item :x="x" :i="i" />
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import ListItem from './components/ListItem.vue'

/* eslint-disable */
export default {
  name: 'app',
  components: {
    ListItem
  },
  data () {
    return {
      items: ['a', 'a', 'a']
    }
  },
  computed: {
    gen () {
      console.log('reactive call anonymous')
      return (x) => {
        console.log('reactive call ' + x)
        return `test${x}`
      }
    },
    comp () {

    }
  },
  methods: {
    append () {
      this.items.push('a')
    }
  }
}
</script>

<style scoped>
.flex {
  display: flex;
}
</style>