<template>
  <v-card
      elevation="12"
      max-width="800"
      class="mx-auto"
  >
    <v-card-title class="pa-1 align-center justify-center card_border">
      <v-icon large color="teal">mdi-chart-bar</v-icon>
      <h2>Skill sets</h2>
    </v-card-title>
    <v-card-text>
      <p class="ma-0 text-center">Levelは1～5でどのぐらい慣れているかの指標です。</p>
      <p class="ma-0 text-center">ライブラリ・エンジンもフレームワークのページに便宜上含めています。</p>
    </v-card-text>
    <v-tabs
        vertical
        :icons-and-text="true"
    >
      <v-tabs-slider></v-tabs-slider>
      <v-tab>
        Languages
        <v-icon large>category</v-icon>
      </v-tab>
      <v-tab>
        Frameworks
        <v-icon large>developer_board</v-icon>
      </v-tab>
      <v-tab>
        Others
        <v-icon large>videogame_asset</v-icon>
      </v-tab>

      <!-- Languages -->
      <v-tab-item>
        <v-card flat>
          <v-simple-table height="432">
            <template v-slot:default>
              <thead>
              <tr>
                <th class="text-left">Language</th>
                <th class="text-center">Level</th>
                <th class="text-center">Detail</th>
              </tr>
              </thead>
              <tbody>
              <tr v-for="item in languages" :key="item.name">
                <td>{{ item.name }}</td>
                <td class="text-center">{{ item.level }}</td>
                <td>{{ item.detail }}</td>
              </tr>
              </tbody>
            </template>
          </v-simple-table>
        </v-card>
      </v-tab-item>

      <!-- Frameworks -->
      <v-tab-item>
        <v-card flat>
          <v-simple-table height="432">
            <template v-slot:default>
              <thead>
              <tr>
                <th class="text-left">Framework</th>
                <th class="text-center">Level</th>
                <th class="text-center">Detail</th>
              </tr>
              </thead>
              <tbody>
              <tr v-for="item in frameworks" :key="item.name">
                <td>{{ item.name }}</td>
                <td class="text-center">{{ item.level }}</td>
                <td>{{ item.detail }}</td>
              </tr>
              </tbody>
            </template>
          </v-simple-table>
        </v-card>
      </v-tab-item>

      <!-- Engines -->
      <v-tab-item>
        <v-card flat >
          <v-simple-table height="432">
            <template v-slot:default>
              <thead>
              <tr>
                <th class="text-left">Name</th>
                <th class="text-center">Level</th>
                <th class="text-center">Detail</th>
              </tr>
              </thead>
              <tbody>
              <tr v-for="item in others" :key="item.name">
                <td>{{ item.name }}</td>
                <td class="text-center">{{ item.level }}</td>
                <td>{{ item.detail }}</td>
              </tr>
              </tbody>
            </template>
          </v-simple-table>
        </v-card>
      </v-tab-item>

    </v-tabs>
  </v-card>
</template>

<script>
  export default {
    name: "SkillSets",
    data () {
      return {
        languages: [
          {
            name: 'Java',
            level: 5,
            detail: '一番頻繁に使っています。JavaFXを使ったアプリケーション開発など。'
          },
          {
            name: 'C#',
            level: 3,
            detail: 'Unity周りで使っています。'
          },
          {
            name: 'HTML5/CSS',
            level: 3,
            detail: '最初に使った言語…？このサイトを作るのに使ってます。'
          },
          {
            name: 'C++',
            level: 2,
            detail: '競プロで使ってます。UE4 C++勉強中です...'
          },
          {
            name: 'Python',
            level: 2,
            detail: '機械学習周りで必要に応じて使います。'
          },
          {
            name: 'PHP',
            level: 2,
            detail: '学部2年次の講義制作にてWebシステムのバックエンドの設計で使用しました。'
          },
          {
            name: 'Javascript',
            level: 2,
            detail: 'こわい'
          },
          {
            name: 'Ruby',
            level: 1,
            detail: 'Rails周りでなんとなーく触りました。'
          }
        ],
        frameworks: [
          {
            name: 'Unity',
            level: 5,
            detail: 'VRのモーションキャプチャシステムからLive2D、ネットワークの実装まで色々。'
          },
          {
            name: 'UE4',
            level: 4,
            detail: '一番好きなゲームエンジン。Arduino自作コントローラによるFPS視点ハクスラ系ゲームの開発など。奥が深すぎてまだまだ未熟者です'
          },
          {
            name: 'JavaFX',
            level: 4,
            detail: 'シューティングゲームの実装など。オブジェクト指向の基礎をこれで学びました'
          },
          {
            name: 'Vue.js',
            level: 3,
            detail: 'このサイトを作るためにだいぶ勉強しました!'
          },
          {
            name: 'Rails',
            level: 2,
            detail: 'RoR5時代に触りました。テスト周りとかは解ります'
          },
          {
            name: 'Flutter',
            level: 1,
            detail: '触りはじめたとこです。スマートフォンアプリ開発用途の予定。'
          },
          {
            name: 'Electron',
            level: 1,
            detail: 'こちらも触りたて。せっかくVue.js勉強したのでデスクトップアプリ開発したい。'
          }
        ],
        others: [
          {
            name: 'Photoshop',
            level: 4,
            detail: 'だいたいよく使う機能は使えます。ポスター制作などで時折使ってます'
          },
          {
            name: 'Illustrator',
            level: 3,
            detail: '最近本腰を据えて触りはじめました。デザイン制作に活用したいです'
          },
          {
            name: 'Cubase 10 Pro',
            level: 3,
            detail: 'DTM用。主に作曲用途、時々効果音作成など。'
          },
          {
            name: 'Clip Studio',
            level: 2,
            detail: '一応持ってますが下手の横好きでお絵かきしてます。'
          },
          {
            name: 'After Effects',
            level: 2,
            detail: '動画編集・エンコーディング用。軽いエフェクトは作れます。'
          }
        ]
      }
    }
  }
</script>

<style scoped>
  .v-icon {
    margin-right: 15px;
  }
</style>