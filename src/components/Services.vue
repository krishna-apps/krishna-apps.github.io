<template>
  <div v-for="(val, i) in services" class="svcContainer" :style="{ background: val.bg }" :key="'uni'+i">
    <div :class="{ flx: true, flxflip: i % 2 }">
      <img :src="val.img" :alt="val.title" />
      <div>
        <h1>{{ val.title }}</h1>
        <ul>
          <li v-for="(item, ind) in val.details" :key="'xy' + ind">{{ item }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props: {
      services: Object
    }
}
</script>
