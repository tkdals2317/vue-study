## 기본 레이아웃 

```Vue
<template>
  <v-app>
    <v-app-bar v-if="$vuetify.breakpoint.xsOnly" app />
    <v-navigation-drawer app />
    <v-main>
      <v-container> 컨텐츠 영역 </v-container>
    </v-main>
    <v-footer app>푸터 영역</v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    drawer: false,
    items: [
      {title: "Dashboard", icon: "mdi-view-dashboard", to: "/"},
      {title: "Grid System", icon: "mdi-image", to: "/grid-system"},
      {title: "Grid List Page", icon: "mdi-image", to: "/grid-list-page"},
    ],
    right: null,
  }),
};
</script>

```

`app` 은 기본 레이아웃이라는 표현하는 속성

`v-main`은 app 속성이 들어있는 기본 레이아웃에 맞춰 컨텐츠 영역의 크기를 조절하게 된다

vue가 마운트 될 때 `v-app-bar`의 높이만큼 `v-main`의 마진이 정해 진다는 느낌

### 🧲 소스코드에서 확인하기    

https://github.com/tkdals2317/Vuetify-Practice/blob/main/src/_App.vue
