
<template>
  <v-app >

    <v-app-bar color="#375472" :elevation="0"  height="50">
      <v-img src="public/theqoo_logo.png" max-height="30" max-width="30" class="mx-3"></v-img>

      <v-btn size="small"  v-if="drawer">전체</v-btn>
      <v-btn size="small"  v-if="drawer">HOT</v-btn>
      <v-btn size="small"  v-if="drawer">스퀘어</v-btn>
      <v-btn size="small"  v-if="drawer">뷰티</v-btn>
      <v-btn size="small"  v-if="drawer">일상토크</v-btn>
      <v-btn size="small"  v-if="drawer">케이돌토크</v-btn>
      <v-btn size="small"  v-if="drawer">드영배</v-btn>
      <v-btn size="small"  v-if="drawer">재펜</v-btn>
      <v-spacer v-if="drawer"></v-spacer>
      <v-text-field
        variant="outlined"
        density="compact"
        :flat="ture"
        bg-color="#6c839f"
        :single-line="true"
        prepend-inner-icon="mdi-magnify"
        placeholder="게시판 찾기"
        hide-details

        @focus="drawer=false"
        @blur="drawer=true"
      />
      <span class="text-body-2 ml-2 mr-2">로그인</span>



    </v-app-bar>
    <v-system-bar class="text-white" color="#6c839f">
      <v-spacer></v-spacer>

      <v-icon class="mr-2">mdi-cog</v-icon>
      내 즐겨찾기 관리
    </v-system-bar>
    <v-main>
      <v-container>
        <RouterView />
      </v-container>
    </v-main>
    <v-footer color="#375472" class="d-flex flex-column">
      <div class="px-4 py-2 text-center w-100">
        © 2012 - 2023 theqoo All rights reserved.
      </div>
      <div class="px-4 py-2 text-center w-100">
        문의메일 : swonjiny@gmail.com
      </div>
    </v-footer>
  </v-app>


<!--  <header>-->
<!--    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />-->

<!--    <div class="wrapper">-->
<!--      <HelloWorld msg="You did it!" />-->

<!--      <nav>-->
<!--        <RouterLink to="/">Home</RouterLink>-->
<!--        <RouterLink to="/about">About</RouterLink>-->
<!--      </nav>-->
<!--    </div>-->
<!--  </header>-->

<!--  <RouterView />-->
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router'
import { ref, watchEffect } from 'vue'

const drawer = ref(true)

window.addEventListener('resize' , () => {
  const width =  window.innerWidth
  drawer.value = width >= 800;
})

watchEffect(()=>{
  const width =  window.innerWidth
  console.log(width)

})
</script>

<style scoped>
.v-input--density-compact {
  --v-input-control-height: 30px;
  --v-input-padding-top: 5px;
  --v-field-padding-top: 0px;
  --v-field-padding-bottom: 0px;
}

</style>
