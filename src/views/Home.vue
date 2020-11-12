<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  data() {
    return {
      cv2: null
    }
  },
  mounted(){
      // As an instance method inside a component
    this.$loadScript("/home/emmanuel/Projects/facile_code/image-labeling/src/assets/js/opencv.js")
      .then(cv2 => {
        // Script is loaded, do something
        console.log("cv2", cv2)
        let mat = cv2.imread()
      })
      .catch(err => {
        // Failed to fetch script
        console.log("err", err)
      });
    
  }
}
</script>
