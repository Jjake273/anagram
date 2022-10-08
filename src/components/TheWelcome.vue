<script>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'

export default {
  data: function() {
    return {
      guess: ''
    }
  },
  methods: {
    async handleClick (){
      console.log(this.guess)
      const response = await fetch('http://localhost:3000', {

    headers: {
      "Content-type": "application/json"
    }

    })
    console.log(response)
  }

}
};
</script>

<template>
  <header>ANAGRAM</header>
  <body>
    <h1>
      Instructions
    </h1>
    <p>
      Here's how to play....
    </p>
    <input type="text" v-model="guess">
    <button @click="handleClick()">button</button>

    
  </body>
</template>
