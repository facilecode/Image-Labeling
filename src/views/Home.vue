<template>
  <div class="home">
    <Labeling></Labeling>
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
import Labeling from '@/components/Labeling.vue'
//import Labeling from '../components/Labeling.vue'

export default {
  name: 'Home',
  components: {
    Labeling
  },
  data() {
    return {
      cv2: null
    }
  },
  mounted(){
     
  }
}
</script>
