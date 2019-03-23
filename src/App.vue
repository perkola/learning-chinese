<template>
  <div class="text-black">
    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->

    <div v-for="radical in radicals" class="flex mt-2 sm:mt-3 mr-2 sm:mr-3">
      <div class="w-1/5 sm:w-1/6 lg:w-1/10 pl-2 sm:pl-3">
        <div class="flex flex-col items-center bg-blue-lighter rounded py-2">
          <span class="text-xl">{{ radical.character }}</span>
          <span class="text-sm text-grey-darker">{{ radical.pinyin }}</span>
          <span class="text-sm text-grey-dark">{{ radical.translation }}</span>
        </div>
      </div>
      <div class="w-4/5 sm:w-5/6 lg:w-9/10 overflow-hidden">
        <carousel :paginationEnabled="false" :scrollPerPage="false" :perPage="4" :perPageCustom="[[576, 5], [992, 9]]">
          <slide v-for="r in radical.related">
            <div class="ml-2 sm:ml-3">
            <div class="flex flex-col items-center w-full bg-white rounded py-2">
              <span class="text-xl">{{ r.character }}</span>
              <span class="text-sm text-grey-dark">{{ r.pinyin }}</span>
              <span class="text-sm text-grey">{{ r.translation }}</span>
            </div>
            </div>
          </slide>
      </carousel>
      </div>
    </div>

    <p class="mt-2 sm:mt-3 p-2 sm:p-3 leading-none bg-white text-sm text-grey-dark">&copy; 2019</p>
  </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel'

export default {
  name: 'app',
  data: function () {
    return {
      components: {
        Carousel,
        Slide
      },
      radicals: [
        {
          character: '女',
          pinyin: 'nǚ',
          translation: 'woman',
          related: [
            { character: '她', pinyin: 'tā', translation: 'her' },
            { character: '好', pinyin: 'hǎo', translation: 'good' },
            { character: '安', pinyin: 'ān', translation: 'calm' },
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
            { character: '信', pinyin: 'xìn', translation: 'letter' },
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
            { character: '森', pinyin: 'sēn', translation: 'forest' },
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
            { character: '早', pinyin: 'zǎo', translation: 'morning' },
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
            { character: '安', pinyin: 'ān', translation: 'calm' },
          ]
        },
        {
          character: '言',
          pinyin: 'yán',
          translation: 'speech',
          related: [
            { character: '信', pinyin: 'xìn', translation: 'letter' },
          ]
        },
        {
          character: '不',
          pinyin: 'bù',
          translation: 'not',
          related: []
        },
        {
          character: '中',
          pinyin: 'zhōng',
          translation: 'middle',
          related: []
        },
        {
          character: '再',
          pinyin: 'zài',
          translation: 'again',
          related: []
        },
        {
          character: '见',
          pinyin: 'jiàn',
          translation: 'see',
          related: []
        },
        {
          character: '也',
          pinyin: 'yě',
          translation: 'too',
          related: []
        },
      ]
    }
  },
}
</script>
