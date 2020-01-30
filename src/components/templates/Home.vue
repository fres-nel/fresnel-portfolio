<template>
  <v-container fluid>
    <v-row
        align="start"
        justify="center"
    >
      <v-col cols="12">
        <!-- Top Icon? -->
        <v-fade-transition mode="out-in">
          <v-card
              elevation="12"
              max-width="500"
              id="top-icon"
              class="mx-auto"
          >
            <!-- TODO アイコン差し替え -->
            <v-img
                max-width="200"
                max-height="200"
                :src="require('@/assets/logo.png')"
                class="mx-auto"
            />
            <v-card-title class="justify-center">
              Welcome my homepage!
            </v-card-title>
          </v-card>
        </v-fade-transition>

        <!-- About me -->
        <v-fade-transition mode="out-in">
          <v-card
              elevation="12"
              max-width="800"
              class="mx-auto"
          >

            <v-card-title class="pa-1 align-center justify-center card_border">
              <v-icon large color="orange">mdi-account</v-icon>
              <h2>About me</h2>
            </v-card-title>
            <v-row
                align="start"
                justify="center"
            >
              <!-- TODO 画像サイズおよびcol数のレスポンシブ対応 -->
              <v-col cols="3" class="pa-3">
                <!-- TODO なんか画像を左右の真ん中にできん -->
                <v-avatar tile size="150" class="mx-auto">
                  <v-img src="https://github.com/fres-nel.png"/>
                </v-avatar>
              </v-col>
              <v-col cols="9" class="pa-3">
                <v-card-text class="pa-0">
                  <p>はじめまして！フレネル(Fresnel)と申します。地方大学の大学院修士1年です。</p>
                  <p>大学入学時(2015年)からプログラミングの勉強を始めてプログラミング歴約5年です。Web開発・ゲーム開発・アプリケーション開発など興味を持った分野を手広くやっています。JavaやUnity,
                    UE4をよく触っています。</p>
                  <p>趣味は温泉めぐりです♨</p>
                </v-card-text>
              </v-col>
            </v-row>
          </v-card>
        </v-fade-transition>
      </v-col>

      <!-- Skill Sets -->
      <v-col cols="12">
        <v-lazy>
          <skill-sets />
        </v-lazy>
      </v-col>

      <!-- Works -->
      <v-col cols="12">
        <v-lazy>
          <Accounts />
        </v-lazy>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  import SkillSets from "@/components/organisms/SkillSets";
  import Accounts from "@/components/organisms/Accounts";
  export default {
    name: "Home",
    components: {Accounts, SkillSets}
  }
</script>

<style scoped>
  #top-icon {
    margin-bottom: 60px;
  }

  .v-card {
    margin-bottom: 50px;
    padding: 10px;
  }

  .v-icon {
    margin-right: 15px;
  }

  .rotate {
    transform: rotateZ(-3deg);
  }

  .rev-rotate {
    transform: rotateZ(2deg);
  }

  .card_border {
    /*border-bottom: #888888 1px solid;*/
  }

  .v-avatar {
    filter: drop-shadow(2px 2px 2px rgba(0, 0, 0, 0.6));
  }
</style>