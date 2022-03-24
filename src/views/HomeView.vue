<template>
  <v-app>
    <v-app-bar v-if="windowSize<900" style="position: fixed;">
      <template v-slot:prepend>
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      </template>

      <v-app-bar-title>Zhou Yubo's Homepage</v-app-bar-title>

<!--      <template v-slot:append>-->
<!--        <v-btn icon="mdi-dots-vertical"></v-btn>-->
<!--      </template>-->
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" :width="windowSize>900?0.3*windowSize:0.8*windowSize" v-bind:[drawerStatue]="true" style="margin-left: 1.5em;margin-top: 1em;position: fixed">
      <v-container>
        <v-card height=50 image="https://images.pexels.com/photos/1323550/pexels-photo-1323550.jpeg?auto=compress&cs=tinysrgb&dpr=2&w=500"></v-card>
        <h1 style="font-size: 2.25em;margin-left: 0.5em;margin-bottom: 0.7em;margin-top: 0.5em">Zhou Yubo</h1>
        <v-btn href="/" variant="plain" prepend-icon="mdi-earth" class="linkBtn">www.albertcamus.xyz</v-btn><br/>
        <v-btn href="mailto:zhou-yubo@qq.com" variant="plain" prepend-icon="mdi-email" class="linkBtn">zhou-yubo@qq.com</v-btn><br/>
        <v-btn href="/Blog" variant="plain" prepend-icon="mdi-microsoft-bing" class="linkBtn">My Blog</v-btn><br/>
        <v-btn href="https://github.com/SherlockZYB" variant="plain" prepend-icon="mdi-github" class="linkBtn">SherlockZYB</v-btn><br/>
        <v-btn class="linkBtn" href="/cv-en.pdf" variant="plain" prepend-icon="mdi-newspaper-variant-outline">CV</v-btn>

        <v-divider></v-divider>

        <v-container>
          <ul style="list-style: none">
            <li>
              <a href="#👻-Personal-Information" class="anchorHref">👻 Personal Information</a>
            </li>
            <li>
              <a href="#📚-Education" class="anchorHref">📚 Education</a>
            </li>
            <ul style="margin-left: 2em;list-style: none">
              <li>
                <a href="#Education-1" class="sub-anchorHref">2019 ~ Present</a>
              </li>
            </ul>
            <li>
              <a href="#👨‍💻-Research-Experience" class="anchorHref">👨‍💻 Research Experience</a>
            </li>
            <ul style="margin-left: 2em;list-style: none">
              <li>
                <a href="#Experience-1" class="sub-anchorHref">2019</a>
              </li>
              <li>
                <a href="#Experience-2" class="sub-anchorHref">2020</a>
              </li>
              <li>
                <a href="#Experience-3" class="sub-anchorHref">2021</a>
              </li>
            </ul>
            <li>
              <a href="#🏆-Awards-&-Scholarships" class="anchorHref">🏆 Awards & Scholarships</a>
            </li>
            <ul style="margin-left: 2em;list-style: none">
              <li>
                <a href="#Bachelor-Period" class="sub-anchorHref">Bachelor Period</a>
              </li>
            </ul>
          </ul>
        </v-container>
      </v-container>
    </v-navigation-drawer>

    <v-main>
      <v-container class="text-center" style="width: 95%;margin-left: 1em">
        <div style="height: 1em"></div>
        <div style="background-color: #f8f8f8 ;height: 20em">
          <div style="width:100%;height: 1.5em"></div>
            <v-avatar size="150">
              <img :src="require('../assets/avatar.jpg')" style="max-height: 100%">
            </v-avatar>
            <h1 style="margin-top: 0.5em;margin-bottom: 0.5em">Zhou Yubo</h1>
            <router-link to="/" replace class="linkBtn" style="color: #2196f3;">English</router-link> | <router-link to="/zh-cn" replace class="linkBtn" style="color: #2196f3;">简体中文</router-link>
        </div>
        <br/>
        <div style="text-align: left">
          <v-btn class="linkBtn" href="/" style="margin-right: 1em;margin-bottom: 1.5em" prepend-icon="mdi-earth">Homepage</v-btn>
          <v-btn class="linkBtn" href="mailto:zhou-yubo@qq.com" style="margin-right: 1em;margin-bottom: 1.5em" prepend-icon="mdi-email">Email</v-btn>
          <v-btn class="linkBtn" href="/Blog" style="margin-right: 1em;margin-bottom: 1.5em" prepend-icon="mdi-microsoft-bing">Blog</v-btn>
          <v-btn class="linkBtn" href="https://github.com/SherlockZYB" style="margin-right: 1em;margin-bottom: 1.5em" prepend-icon="mdi-github">Github</v-btn>
          <v-btn class="linkBtn" href="/cv-en.pdf" style="margin-right: 1em;margin-bottom: 1.5em" prepend-icon="mdi-newspaper-variant-outline">CV</v-btn>
        </div>
      </v-container>
      <v-container style="width: 95%">
        <p class="contentHeader" id="👻-Personal-Information">👻 Personal Information</p>
        <v-divider></v-divider><br/>
        <p class="infoContent">Zhou Yubo is now a third-year student in <a class="innerLink" href="https://www.scu.edu.cn/">Sichuan University</a>, China.
          In June, 2020, he became an intern of <a class="innerLink" href="http://scuvis.org/">SCU VIS Lab</a> under Professor <a class="innerLink" href="https://cs.scu.edu.cn/info/1359/16768.htm">Zhu Min</a>.
          Inspired by his mentor and other students in the Lab, his has strong interests in visualization, visual analytics and AR/VR. </p>
        <v-container style="margin-left: 0.3em;">
          <ul>
            <li><p>My Blog: <a class="innerLink" href="/Blog">Baker Street 221B</a></p></li>
            <li><p>Github: <a class="innerLink" href="/">SherlockZYB</a></p></li>
          </ul>
        </v-container>


        <p class="contentHeader" id="📚-Education">📚 Education</p>

        <v-divider></v-divider><br/>

        <p><a class="innerLink" href="#Education-1" id="Education-1" style="font-size: 1.2em">2019 ~ Present</a><h4 style="display:inline-block;float:right">Sichuan University</h4></p>
        <p>Major: Computer Science and Technology</p>
        <v-container style="margin-left: 0.3em;">
          <ul>
            <li><p>College: College of Computer Science and Technology</p></li>
          </ul>
        </v-container>
        <p>Minor: Comprehensive Training Programme for Innovative Talents</p>
        <v-container style="margin-left: 0.3em;">
          <ul>
            <li><p>College: Wu Yuzhang Honours College</p></li>
          </ul>
        </v-container>

        <p class="contentHeader" id="👨‍💻-Research-Experience">👨‍💻 Research Experience</p>
        <v-divider></v-divider><br/>
        <p><a class="innerLink" href="#Experience-1" id="Experience-1" style="font-size: 1.2em">2019</a></p>
        <p style="">Development of a virtual simulation experimental platform for fall simulation and risk assessment of the elderly based on the PEO model</p>
        <v-container style="margin-left: 0.3em;">
          <ul>
            <li><p>Type: College Students' Innovative Entrepreneurial Training Plan Program - Provincial</p></li>
            <li><p>Details: Implementing core functions (Process control, Question & Answer, etc. | based on Unity3D), creating character animations (based on 3DS Max), writing project documentation, presentation and defense.</p></li>
          </ul>
        </v-container>
        <p style="">"Sui Xin Fen" - A convolutional neural network based rubbish recognition and classification encouragement app</p>
        <v-container style="margin-left: 0.3em;">
          <ul>
            <li><p>Type: College Students' Innovative Entrepreneurial Training Plan Program - University</p></li>
            <li><p>Details: None.</p></li>
          </ul>
        </v-container>
        <p><a class="innerLink" href="#Experience-2" id="Experience-2" style="font-size: 1.2em">2020</a></p>
        <p style="">Development of a virtual simulation system for first aid training for caregivers in elderly institutions - an example of choking protection for the elderly</p>
        <v-container style="margin-left: 0.3em;">
          <ul>
            <li><p>Type: College Students' Innovative Entrepreneurial Training Plan Program - Provincial</p></li>
            <li><p>Details: Implementing core functions (Timing and scoring, Database synchronisation, etc. | based on Unity3D), acquiring sensor data (related to IoT), deploying to Web, applying software copyright, utility model patent.</p></li>
          </ul>
        </v-container>
        <p style="">Application of generative adversarial network-based image alignment techniques in the follow-up of jaw cyst disease</p>
        <v-container style="margin-left: 0.3em;">
          <ul>
            <li><p>Type: College Students' Innovative Entrepreneurial Training Plan Program - College</p></li>
            <li><p>Details: None.</p></li>
          </ul>
        </v-container>
        <p><a class="innerLink" href="#Experience-3" id="Experience-3" style="font-size: 1.2em">2021</a></p>
        <p style="">Development of Agricultural shed information management platform</p>
        <v-container style="margin-left: 0.3em;">
            <ul>
                <li><p>Type: Research and development of practical curriculum projects</p></li>
                <li><p>Details: Integration and division of labour, writing project documentation (requirements, testing, design, etc.), web development(3 modules).</p></li>
            </ul>
        </v-container>
        <p class="contentHeader" id="🏆-Awards-&-Scholarships">🏆 Awards & Scholarships</p>
        <v-divider></v-divider><br/>
        <p><a class="innerLink" href="#Bachelor-Period" id="Bachelor-Period" style="font-size: 1.2em">Bachelor Period</a></p>
        <v-container style="margin-left: 0.3em;">
          <ul>
              <li><p>Sichuan University Comprehensive Second-Class & Third-Class Scholarship</p></li>
              <li><p>Outstanding Student of Sichuan University</p></li>
              <li><p>2021 Asia and Pacific Mathematical Contest in Modeling Second Prize</p></li>
          </ul>
        </v-container>
      </v-container>

    </v-main>
  </v-app>
</template>

<script>
import { defineComponent,ref } from 'vue';

// Components
import HelloWorld from '../components/HelloWorld.vue';

export default defineComponent({
  name: 'HomeView',
  components: {
  },
  setup(){
    let windowSize=ref(document.body.clientWidth)
    let scrollTop=ref(0)
    let drawer=ref(true)
    let drawerStatue=ref('permanent')

    window.onresize=()=>{
      windowSize.value=document.body.clientWidth
      if(windowSize.value>900){
        drawer.value=true
        drawerStatue.value='permanent'
      }else {
        drawer.value=false
        drawerStatue.value='temporary'
      }
    }

    window.onscroll=()=>{
      scrollTop.value = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop

    }

    return {windowSize,scrollTop,drawer,drawerStatue}
  }
});
</script>

<style>
  body{
    font-family: Adele;
  }
  p{
    color: #34495e;
    font-size: 1.2em;
    line-height: 1.5em;
  }
  .contentHeader{
    font-size: 1.6em;
  }
  h1{
    color: #34495e;
  }
  li{
    margin: 0.5em;
  }
  .innerLink{
    color: #2d99b8;
  }
  .linkBtn{
    font-size: 1em;
    text-transform: none;
    text-decoration: none;
    margin-top:-0.8em;
  }
  .linkBtn:hover{
    color: #2d99b8;
  }
  .anchorHref{
    color: #34495e;
    font-size: 1.3em;
    text-decoration: none;
    text-underline: none;
  }
  .sub-anchorHref{
    color: #34495e;
    font-size: 1.2em;
    text-decoration: none;
    text-underline: none;
  }
  /*定义滚动条高宽及背景
 高宽分别对应横竖滚动条的尺寸*/
  ::-webkit-scrollbar
  {
    width:0.5em;
    height:0.5em;
    background-color:#F5F5F5;
  }
  /*定义滚动条轨道
   内阴影+圆角*/
  ::-webkit-scrollbar-track
  {
    -webkit-box-shadow:inset 0 0 6px rgba(0,0,0,0.3);
    border-radius:10px;
    background-color:#F5F5F5;
  }
  /*定义滑块
   内阴影+圆角*/
  ::-webkit-scrollbar-thumb
  {
    border-radius:10px;
    -webkit-box-shadow:inset 0 0 6px rgba(0,0,0,.3);
    background-color: #959595;
  }
</style>
