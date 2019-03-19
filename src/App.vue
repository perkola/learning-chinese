<template>
  <div class="px-3 text-black">
    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->

    <div v-for="radical in radicals" class="flex mt-3">
      <div class="flex flex-col items-center w-16 bg-blue-lighter rounded py-2">
        <span class="text-xl">{{ radical.character }}</span>
        <span class="text-sm text-grey-darker">{{ radical.pinyin }}</span>
        <span class="text-sm text-grey-dark">{{ radical.translation }}</span>
      </div>
      <div v-for="r in radical.related" class="flex flex-col items-center w-16 bg-white rounded py-2 ml-3">
        <span class="text-xl">{{ r.character }}</span>
        <span class="text-sm text-grey-dark">{{ r.pinyin }}</span>
        <span class="text-sm text-grey">{{ r.translation }}</span>
      </div>
    </div>

    <p class="py-3 text-sm text-grey-dark">&copy; 2019</p>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  data: function () {
    return {
      radicals: [
        {
          character: '女',
          pinyin: 'nǚ',
          translation: 'woman',
          related: [
            { character: '她', pinyin: 'tā', translation: 'her' },
            { character: '好', pinyin: 'hǎo', translation: 'good' },
          ]
        },
        {
          character: '人 亻',
          pinyin: 'rén',
          translation: 'man',
          related: [
            { character: '他', pinyin: 'tā', translation: 'him' },
            { character: '你', pinyin: 'nǐ', translation: 'you' },
            { character: '什', pinyin: 'shén', translation: 'what' },
          ]
        },
        {
          character: '水 氵',
          pinyin: 'shuǐ',
          translation: 'water',
          related: [
            { character: '酒', pinyin: 'jiǔ', translation: 'wine' },
          ]
        },
        {
          character: '口',
          pinyin: 'kǒu',
          translation: 'mouth',
          related: [
            { character: '国', pinyin: 'guó', translation: 'country' },
            { character: '叫', pinyin: 'jiào', translation: 'to call' },
            { character: '吃', pinyin: 'chī', translation: 'to eat' },
            { character: '喝', pinyin: 'hē', translation: 'to drink' },
          ]
        },
        {
          character: '木',
          pinyin: 'mù',
          translation: 'tree',
          related: [
            { character: '桃', pinyin: 'táo', translation: 'peach' },
            { character: '梨', pinyin: 'lí', translation: 'pear' },
          ]
        },
        {
          character: '大',
          pinyin: 'dà',
          translation: 'big',
          related: []
        },
        {
          character: '刀 刂',
          pinyin: 'dāo',
          translation: 'knife',
          related: [
            { character: '梨', pinyin: 'lí', translation: 'pear' },
          ]
        },
        {
          character: '子',
          pinyin: 'zǐ',
          translation: 'child',
          related: [
            { character: '好', pinyin: 'hǎo', translation: 'child' },
            { character: '字', pinyin: 'zì', translation: 'character' },
          ]
        },
        {
          character: '们',
          pinyin: 'mén',
          translation: 'gate',
          related: []
        },
        {
          character: '日',
          pinyin: 'rì',
          translation: 'sun',
          related: [
            { character: '是', pinyin: 'shì', translation: 'is are am' },
          ]
        },
        {
          character: '亠',
          pinyin: 'tóu',
          translation: 'lid',
          related: []
        },
        {
          character: '宀',
          pinyin: 'mián',
          translation: 'roof',
          related: [
            { character: '字', pinyin: 'zì', translation: 'character' },
          ]
        },
      ]
    }
  },
  components: {
    HelloWorld
  }
}
</script>
