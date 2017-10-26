<template>
  <div class="g-mn">
    <!--背景-->
    <div class="s-bg">
      <div class="s-bgi"></div>
      <div class="s-bgc"></div>
    </div>
    <div class="m-box">
      <div class="m-mn j-mn">
        <div class="m-mnc u-tt-mn">
          <p class="u-tt-name">{{info.surname}}<span class="u-tt-span">{{info.name}}</span>.</p>
          <p class="u-tt-p">{{info.tips}}</p>
        </div>
        <div v-for="data in home">
          <div class="m-mnc u-mu" v-if="data.type == 'text'">
            <i v-bind:class="data.icon"></i>
            <span class="u-mnc-tips">{{data.text}}</span>
          </div>
          <div class="m-mnc u-bgi" v-if="data.type == 'img'">
            <img class="u-bgi-img" v-bind:src="data.img" />
          </div>
          <div class="m-mnc u-null brick" v-if="data.type == 'null'" v-on:click="k()">ss</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data () {
      return {
        info: {
          surname: 'JIANG',
          name: 'YALIN',
          tips: 'Lovely is the truth, Adorable is justice.'
        },
        home: [
          {
            type: 'text',
            icon: 'fa fa-home',
            text: 'Personal Website',
            href: '/'
          }, {
            type: 'img',
            img: './../../static/home/ui-01.png'
          }, {
            type: 'null'
          }, {
            type: 'text',
            icon: 'fa fa-video-camera',
            text: 'Video',
            href: '/'
          }, {
            type: 'text',
            icon: 'fa fa-book',
            text: 'Cartoon',
            href: '/'
          }, {
            type: 'img',
            img: './../../static/home/ui-02.png'
          }, {
            type: 'img',
            img: './../../static/home/ui-03.png'
          }, {
            type: 'text',
            icon: 'fa fa-picture-o',
            text: 'Picture',
            href: '/'
          }, {
            type: 'img',
            img: './../../static/home/ui-04.png'
          }, {
            type: 'null'
          }, {
            type: 'img',
            img: './../../static/home/ui-05.png'
          }, {
            type: 'null'
          }, {
            type: 'null'
          }, {
            type: 'text',
            icon: 'fa fa-music',
            text: 'Music',
            href: '/'
          }
        ]
      }
    },
    methods: {
      k: function () {
        console.log('ppp')
      }
    }
//    mounted() {
//      window.onresize = function temp() {
//        console.log('dddd')
//      }
//    }
  }
</script>

<style>
  @import "./../assets/home/home.scss";
</style>
