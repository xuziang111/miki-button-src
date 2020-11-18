<template>
  <div id="app">
        <Modal></Modal>
        <nav class="navbar navbar-default navbar-fixed-top">
            <div class="container-fluid" id="top-header">
                <div class="navbar-header">
                    <!-- <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-navbar-collapse" aria-expanded="false">
                        <span class="sr-only">{{ $t("action.toggleNavbar") }}</span>
                    </button> -->
                    <a class="navbar-brand" href="/"><div>{{ $t("info.title") }}</div></a>
                </div>
                <div class="brand1">
                    <a href="https://space.bilibili.com/477317922/" target="_blank"><img src="resources/bilibili.svg" title="B站链接" alt="B站链接" height="18"/></a>
                </div>
                <div class="brand1">
                    请注意音量大小
                </div>
                <div class="brand1">
                    <a href="https://www.bilibili.com/video/BV11D4y1d7wm/" target="_blank">点我听歌</a>
                </div>
                <div class="brand1">
                    <!-- 不留遗憾 -->
                    <!-- 相信一切都会好起来 -->
                </div>
                <!-- <div class="collapse navbar-collapse" id="bs-navbar-collapse">
                    <ul class="nav navbar-nav">
                        <li><a href="https://space.bilibili.com/477317922/" target="_blank"><img src="resources/bilibili.svg" height="18"/></a></li>
                    </ul>
                    <ul class="nav navbar-nav navbar-right">
                        <li class="dropdown">
                            <a href="javascript:;" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">{{$t("lang." + currentLang)}} <span class="caret"></span></a>
                            <ul class="dropdown-menu">
                                <li><a href="javascript:;" @click="chlang('zh-CN')">{{$t("lang.zh-CN")}}</a></li>
                                <li><a href="javascript:;" @click="chlang('en-US')">{{$t("lang.en-US")}}</a></li>
                                <li><a href="javascript:;" @click="chlang('ja-JP')">{{$t("lang.ja-JP")}}</a></li>
                            </ul>
                        </li>
                    </ul>
                </div> -->
            </div>
        </nav>
        <div class="container-fluid main-content">
            <HomePage></HomePage>
            <!-- <div class="container-fluid img-center" >
                <img src="resources/yanhuo.gif">
            </div>  -->
            <!-- <div :class=xxx >
                <img src="resources/mikid.png">
            </div>  -->
            <div class="fixed-left" >
                <img src="resources/mi.png">
            </div> 
        </div>
        <footer class="footer">
                <div>
                    <div>{{$t("info.audioStaff")}}</div>
                    <div>友情链接:<a href="https://www.mihiru.com" target="_blank">mihiru.com</a>&nbsp;
                    <a href="https://mahiru-vr.github.io/" target="_blank">孟按钮</a> &nbsp;
                    <a href="https://bbs.nga.cn/read.php?tid=23498962" target="_blank">NGA弥楼</a> &nbsp;
                    <a href="https://bbs.nga.cn/read.php?tid=23130748" target="_blank">告一段落的病栋</a> &nbsp;
                    </div>
                    <div>音频投稿:touhou@lolimy.cn github 或者弥四/魔球群丢群文件 只有时间点也行</div>
                </div>
                <div>
                    <div class="text-right"><a href="https://github.com/zyzsdy/aqua-button" target="_blank">原项目</a></div>
                    <div class="text-right">本项目<a href="https://github.com/xuziang111/miki-button-src" target="_blank">{{$t("info.toGithub")}}</a></div>
                    <div class="text-right">{{$t("info.notOfficial")}}</div>
                </div>
                <!-- <div>Zyzsdy 2019-2020 <span style="color: rgba(0, 0, 0, 0.1)">Powered By Meowsound Idols</span></div> -->
        </footer>
  </div>
</template>

<style lang="scss">
@import "../node_modules/bootstrap/dist/css/bootstrap.css";
.cate-header{
    color:#fff;
}
#top-header{
    display:flex;
}
.fixed-left{
    position: fixed;
    z-index: -1;
    top:10px;
    right:0;
}
.fixed-left img{
    // position: absolute;
    // z-index: -1;
    // top:0;
    // right:0px;
    // width:50%;
    height:100vh;
}
.img-left{
    position: fixed;
    z-index: -1;
    top:0;
    right:-100px;
}
.img-center2{
    position: fixed;
    z-index: -1;
    
    top:0;
    right:-300px;
}
.img-center2 img{
    width:100%;
}
.img-center{
    display:flex;
    justify-content: center;
    padding:10px 0 10px 0;
}
.brand1{
    padding:0 5px 0 5px;
    display:flex;
    justify-content: center;
    align-items: center;
}
html{
    height:100%;
}
body{
    padding-top: 70px;
    height:100%;
}
#app{
    min-height:100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.main-content{
    // min-height: 100vh;
}
.footer {
    width: 100%;
    background-color: #ebebeb;
        display:flex;
    padding: 10px;
    color: #666;
    justify-content:space-between;
    align-items: center;
}
// .footer-content {
//     display:flex;
//     padding-top: 10px;
//     color: #666;
//     justify-content:space-between;
//     align-items: center;
// }
.text-right{
    text-align: right;
}
</style>

<script>
import Vue from 'vue'
import Component from 'vue-class-component'
import Modal from './components/modal.vue'
import HomePage from './components/home.vue'
//import fetchpost from './util/fetchpost'

@Component({
    components:{
        Modal,
        HomePage
    }
})
class App extends Vue {
    get currentLang(){
        return this.$i18n.locale;
    }
    data(){
        return {
            xxx:'container-fluid img-left'
        }
    }
    created(){
        // eslint-disable-next-line 
        console.log("                             ;&@@@@@@|`\n                           !&&&&&&&&&&&%'\n                         `|$$%$%%%$$$$$$$:\n                         !$$$$$%%$$$$&&&&%`\n                        '%$$$%%$$$;;%$$$&$'\n                        :$$$!`'|$!` .!%$&$'\n                        ;&$%!%%!!'.:|||$$%'\n                        ;&$%'        .!$&|.\n                        `|$&%'      .!&&$;\n                         `!&&&$;. .;$&&$!\n                          .:|&$|:'';$@@$'\n                          .!&@|'````!@&&|`\n                       ;&$$$&$:`|&!.;&@@&$&|.\n                      ;&$%$&$$!'!|':%&&&&$&&|`\n                     !&$$$&$$%!!$$!;|$&&&&&$&!.  \n                    !&$%&@&$&%!!!!;!%&&&&@@&$&|`  \n                 `|$$%&@@&&&%!!!!!!%&&@@&&&&&&%`  \n                '%$$%$|:%@&&$|!||!!%&&%%|`;&&&&&:    \n               ;&&$%%' `%&@@$||!|!!$@&&@|. '$@&&&!    \n              !&&$$!   `%&@&%||||!!$@&&&|.   !@@&&%` \n              ;$$$&@|. '$&&&$%$$%%%$@&&&&: :$&&&&&!   \n               `%&$$$&&&&&&$|!!||||$&&&@&$&$$$&&!   \n           .. :!..!$&||@&&&$%%%|%%$$&&&@%|&&$$!   \n       .`     :|'   '|&&$$&%|%|!|%%$&&&&&!!$:   \n     .`       '%$&&;`|&$$&$|!||!|||%$$&&@|.`'   \n    ``        '||%|;|&&$$&%|||!!!||%&&&&&$:.;|'   \n   ``         ;||%$&&&$$$$%!|!!!!||%&&&$&&@@@&%:``..  \n   `.        '|%%%$&&&$$&$|!|!!!|||%$&&&&&&%%%||;:!'`.  \n  .'...   . '!%%%:!&$$$&&$|!||!!||||$&&&&&&&$$%%!:||;'  \n  `'``.....'|$$%;'|$%||||!!!||!!|||||||%%%$$$%%%%|%$%'  \n  .'``````;$&&$$$$&%%|!||!!!|!!!||||||||%%$$&$%%$%:  \n   .::';|$&@@@@&&&$|||!||!!||!!!!|||||||%%%$$&$%|!`  \n       ;$&@@@@@@&$|||!!!!!!||!!!!|||||||%%%%$$$&$||;.  \n          .!%%|!|||||!!!!!!||!!!!||||||||%%%%$$%%%;  \n                :|||!!!!!!!||!!!!||!|||||%%%%%!`    \n                :|||!!|!!!!|!!!!!||!|||||%%|%%!.  \n               '|||!!||!!!!|!!!!!||!!|||||%|%%%:    \n              .;|||!!||!!!!!!!!!!||!!|||||%%|%%|'  \n              '|%||!|||!!!!|!!!!!||!!|||||%%|%%$!. \n             .!%%||||%|!!!||!!!!!||!|||||||%|%%$$:  \n             `|%%||||%|||||||||||||||||%|||%%%%$!. \n                :|||%%|||||%|||||%%|||||%||%%;`    \n                     ';!!!!|%|!!;;||!!!;;:'`     \n                    .'''':'           `::'''.    \n                    `:''''`           .:''''`    \n                    .`''''`           .'''`..    \n                    .    .             .     .  \n                    .    .             .     .  \n                    .    .             .     .    \n                    .    .             .     .  \n                     .   .              .    .     \n                    :'  .'.             ::  .;'  \n                    ;$$$&%`             :$$$&%'  \n                    :$$$&|.             '$&&&%`  \n                     !&&&;               ;&&&!   \n                     :$&&;               :$&&;   \n                     .|&&;               '$&&:   \n                     .|@@|.              '$@@;   \n                     '$@@@;              !@@@|.  \n                     `|&&&;             '%&&&%`  \n                     :$$$$%'           :$$$$&!   \n                     :;.  ``          .`  `|$'   \n                      .....            `...`.     \n早知道女孩子也会被 女人配不上我 弥希miki是没有未来的 咳嗽X 伸懒腰X mahiru主人")
        // console.log("10/12饿啊 结果miki真的就从头到尾没变过 920后也没变过 真的是太扭曲了")
        // console.log("观众不要试图去改变演员想法，特别还是虚拟的（")
        //早知道女孩子也会被 女人配不上我 弥希miki是没有未来的 咳嗽X 伸懒腰X mahiru主人
        this.$i18n.locale = localStorage.getItem("lang") || this.$i18n.locale;
    }
    mounted(){
        if(document.body.clientWidth<768){
            this.xxx = 'container-fluid img-center2'
        }
    }
    chlang(v){
        this.$i18n.locale = v;
        localStorage.setItem("lang", v);
    }
}

export default App;
</script>

