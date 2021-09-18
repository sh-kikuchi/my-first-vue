<template>
  <v-card flat>
    <v-card-text>
      <p>きくち/kikuchi<font-awesome-icon icon="coffee" /></p>
      <ul>
        <li>1994年7月26日、獅子座</li>
        <li>趣味：外出ること、ライブ参戦、たまにインラインスケート</li>
      </ul>
      <p>
        「何もないことは何でもありってこと」って誰かが言っていたことをそのまま丸呑みして、IT業界に飛び込んだものの、継続してスキルを磨くことはやっぱり大変。これまで、何だかんだでサーバーサイド言語に触れる機会が多かったけど、実はWebサイトやアプリのUIの実装に興味があって、フロントエンドも良さげなものを触りたいと思っていました。そこで手を出したのがVue.js。本サイトはVue.jsで作られているけれど、基礎を理解するまでに半年以上もかかってしまうという体たらく。そう、フロント慣れしていないものでなかなか…、ね？最近はユニットを組んでアプリ制作をしたいなと思ってます。
      </p>
      <h3 class="text-center text-h6">Skills</h3>
      <hr />
      <div class="pg-lang text-center">
        <span><font-awesome-icon :icon="['fab', 'html5']" />HTML5・ </span>
        <span><font-awesome-icon :icon="['fab', 'css3']" />CSS3・ </span>
        <span
          ><font-awesome-icon :icon="['fab', 'js']" />JavaScript/JQuery・
        </span>
        <span
          ><font-awesome-icon :icon="['fab', 'bootstrap']" />Bootstrap・
        </span>
        <span><font-awesome-icon :icon="['fab', 'php']" />PHP7・ </span>
        <span
          ><font-awesome-icon :icon="['fab', 'laravel']" />Laravel(5.5-8)・
        </span>
        <span><font-awesome-icon icon="database" />MySQL/SQLserver・ </span>
        <span
          ><font-awesome-icon :icon="['fab', 'vuejs']" />Vue.js(2.x)・
        </span>
        <span><font-awesome-icon :icon="['fab', 'markdown']" />Markdown </span>
      </div>
      <div>
        <v-btn color="Black d-block mt-5 mx-auto" dark>
          <a href="https://github.com/sh-kikuchi" class="btn-github"
            ><font-awesome-icon
              :icon="['fab', 'github']"
              class="mr-2"
            />GitHub</a
          >
        </v-btn>
      </div>
      <br />

      <h3 class="text-center text-h6">Works</h3>
    </v-card-text>

    <div class="d-md-flex flex-direction:start">
      <v-card class="mx-auto" max-width="344" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <div class="text-overline mb-4">個人サイト</div>
            <v-list-item-title class="text-h5 mb-1">
              mysite -Into the Wild-
            </v-list-item-title>
            <v-list-item-subtitle
              >HTML,CSS,JavaScript/jQuery,MySQL,PHP</v-list-item-subtitle
            >
          </v-list-item-content>
        </v-list-item>
        <v-card-text>
          自分にフィットする本や音楽、そして旅行という逃避行（笑）など、プライベート感が爆発しているサイト。それに加えて、学生時代に研究していた日本近現代史をまとめたページもあり、研究成果を発表しています。因みにサイト名に使われている「Into
          the Wild」はGLAYER故。
        </v-card-text>
      </v-card>
      <v-card class="mx-auto" max-width="344" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <div class="text-overline mb-4">toolboxシリーズ</div>
            <v-list-item-title class="text-h5 mb-1"> kanban </v-list-item-title>
            <v-list-item-subtitle
              >Laravel8（5.5~）,jQuery,MySQL,HTML,CSS</v-list-item-subtitle
            >
          </v-list-item-content>
        </v-list-item>
        <v-card-text>
          アプリで「お道具箱」をつくるコンセプトで始めた自主企画ものが「toolbox」です。第1弾がトレロ風かんばんアプリです。個人向けのタスク管理で、wiki機能も搭載。並べ替えは出来るようにしましたが、本家のようにドラッグアンドドロップは出来ませんので悪しからず。緑を基調としたデザイン。(email:test@test.com
          password:testtest ※パスワード変更はしないで下さい)
        </v-card-text>
        <v-card-actions>
          <v-btn outlined rounded text
            ><a href="http://sk-kanban.herokuapp.com/"> アプリへ移動 </a></v-btn
          >
        </v-card-actions>
      </v-card>
      <v-card class="mx-auto" max-width="344" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <div class="text-overline mb-4">toolboxシリーズ</div>
            <v-list-item-title class="text-h5 mb-1">
              smalltalk
            </v-list-item-title>
            <v-list-item-subtitle
              >Laravel8（6~）,Bootstrap,jQuery,MySQL,HTML,CSS</v-list-item-subtitle
            >
          </v-list-item-content>
        </v-list-item>
        <v-card-text>
          「toolbox」第2弾。TwitterのようなSNSアプリ。「お茶の間」トークを楽しめるように、つぶやきに対してのコメント機能を実装しました。でもたまには一人で居たいよね。。そんな時には「ひとりごと」という場所で独り言を呟けます←必要か？
          青を基調としたデザイン。
        </v-card-text>
        <v-card-actions>
          <v-btn outlined rounded text>非公開</v-btn>
        </v-card-actions>
      </v-card>
      <v-card class="mx-auto" max-width="344" outlined>
        <v-list-item three-line>
          <v-list-item-content>
            <div class="text-overline mb-4">toolboxシリーズ</div>
            <v-list-item-title class="text-h5 mb-1">
              bookstock
            </v-list-item-title>
            <v-list-item-subtitle
              >Laravel8,Bootstrap,jQuery,MySQL,HTML,CSS</v-list-item-subtitle
            >
          </v-list-item-content>
        </v-list-item>
        <v-card-text>
          「toolbox」第3弾はブックメモアプリ。自分で決めたテーマ毎に本の要約や引用をまとめられるもの。「自分が学生時代にレポートやレジュメを作成する中であったら便利だったな」という思いでつくってみました。複数の本から情報をまとめたい時には是非。赤を貴重としたデザイン
        </v-card-text>
        <v-card-actions>
          <v-btn outlined rounded text
            ><a href="http://sk-bookstock.herokuapp.com/">
              アプリへ移動
            </a></v-btn
          >
        </v-card-actions>
      </v-card>
    </div>
  </v-card>
</template>
<script>
export default {
  name: "PersonalWork",
};
</script>
<style scoped>
a {
  text-decoration: none;
}

.pg-lang {
  font-size: 16px;
}

.btn-github {
  text-decoration: none;
  color: white;
}
</style>
