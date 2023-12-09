<script setup lang="ts">
const subList = [
  { id: 1 , name: '방송플렛폼', sid : 1 , top : 1  },
  { id: 2 , name: '공기', sid : 2 , top : 0  },
  { id: 3 , name: '문의/신고', sid : 2 , top : 0  },
  { id: 4 , name: '문제보고', sid : 2 , top : 0  },
  { id: 5 , name: '테스트/메모장', sid : 2 , top : 0  },
  { id: 6 , name: '전체', sid : 3 , top : 0  },
  { id: 7 , name: '오우야', sid : 3 , top : 0  },
  { id: 8 , name: '스퀘어', sid : 3 , top : 0  },
  { id: 9 , name: '코로나19', sid : 3 , top : 0  },
  { id: 10 , name: '일상토코', sid : 4 , top : 0  },
  { id: 11 , name: '해외거주토크', sid : 4 , top : 0  },
  { id: 12 , name: '후기', sid : 4 , top : 0  },
  { id: 13 , name: '건강', sid : 4 , top : 0  },
  { id: 14 , name: '공부', sid : 4 , top : 0  },
  { id: 15 , name: '자취', sid : 4 , top : 0  },
  { id: 16 , name: '직장인', sid : 4 , top : 0  },
  { id: 17 , name: '주식', sid : 4 , top : 0  },
  { id: 18 , name: '연예', sid : 4 , top : 0  },
  { id: 19 , name: '자동차/대중교통', sid : 4 , top : 0  },
  { id: 20 , name: '케이돌토크', sid : 5 , top : 0  },
  { id: 21 , name: '힙합', sid : 5 , top : 0  },
  { id: 22 , name: '락/밴드', sid : 5 , top : 0  },
  { id: 23 , name: '드영배', sid : 5 , top : 1  },
  { id: 24 , name: '-그 남자의 기억법', sid : 5 , top : 0  },
  { id: 25 , name: '-더 킹 : 영원의 군주', sid : 5 , top : 0  },
  { id: 26 , name: '-브람스를 좋아하세요?', sid : 5 , top : 0  },
  { id: 27 , name: '-빈센조', sid : 5 , top : 0  },
  { id: 28 , name: '-사랑의 불시착', sid : 5 , top : 0  },
  { id: 29 , name: '-사이코지만 괜찮아', sid : 5 , top : 0  },
  { id: 30 , name: '-스토브리그', sid : 5 , top : 0  },
  { id: 31 , name: '-어쩌다 발견한 하루', sid : 5 , top : 0  },
  { id: 32 , name: '-한 번 다녀왔습니다', sid : 5 , top : 1  },
  { id: 33 , name: '예능', sid : 5 , top : 1  },
  { id: 34 , name: '나는 SOLO', sid : 5 , top : 0  },
  { id: 35 , name: '-남의연애2', sid : 5 , top : 0  },
  { id: 36 , name: '최강야구', sid : 5 , top : 2  },
  { id: 37 , name: '-프로듀스48', sid : 5 , top : 0  },
  { id: 38 , name: '-프로듀스101 시즌2', sid : 5 , top : 0  },
  { id: 39 , name: '-팬텀싱어', sid : 5 , top : 0  },
  { id: 40 , name: '-피크타임', sid : 5 , top : 0  },
  { id: 41 , name: '-환승연애2', sid : 5 , top : 0  },
  { id: 42 , name: '재팬', sid : 6 , top : 0  },
  { id: 43 , name: '일드영배', sid : 6 , top : 0  },
  { id: 44 , name: '차이나', sid : 6 , top : 0  },
  { id: 45 , name: '웨스트(WEST)', sid : 6 , top : 0  },
  { id: 46 , name: '태국', sid : 6 , top : 0  },
  { id: 47 , name: 'WORLD', sid : 6 , top : 0  },
  { id: 48 , name: '스포츠종합', sid : 7 , top : 1  },
  { id: 49 , name: '국내야구', sid : 7 , top : 0  },
  { id: 50 , name: '해외야구', sid : 7 , top : 0  },

]

const categoryList = [
  {id : 1 , name: '신규카테'},
  {id : 2 , name: '송쿠'},
  {id : 3 , name: '유머/이슈/정보'},
  {id : 4 , name: '생활'},
  {id : 5 , name: '국내연예'},
  {id : 6 , name: '스포츠'},
  {id : 7 , name: '취미'},
  {id : 8 , name: '뷰티/팬션'},
  {id : 9 , name: '음식'},
  {id : 10 , name: '컬쳐'},
  {id : 11 , name: '게임'},
  {id : 12 , name: '기타'},
  {id : 13 , name: '케이스타'},
  {id : 14 , name: '케이스타'},
  {id : 15 , name: '케이스타'},
  {id : 16 , name: '케이스타'},
  {id : 17 , name: '케이스타'},
  {id : 18 , name: '케이돌-Boys-'},
  {id : 19 , name: '케이돌-Boys-'},
  {id : 20 , name: '케이돌-Girls-'},
  {id : 21 , name: '케이돌-Girls-'},
  {id : 22 , name: '케이돌-Girls-'},
  {id : 23 , name: '케이돌-Girls-'}
]

</script>

<template>
  <v-row no-gutters >
    <v-col cols="12" md="2" sm="4" v-for="(item, index) in  categoryList" :key="index" >
      <v-table density="compact" class="mb-3" >
        <thead style="background-color: #2c3e50" class="text-white" >
        <tr >
          <th class="text-left">
            {{item.name}}
          </th>
        </tr>
        </thead>
        <tbody>
        <tr
          v-for="sitem in subList"
          :key="sitem.name"
          style="font-size: smaller"
        >
          <td v-if="sitem.sid === item.id">
            <span style="font-weight: bolder" v-if="sitem.top === 2" > [new]</span>
            <span :style="{'font-weight' : sitem.top > 0 ? 'bolder' : ''}">
              <v-icon v-if="sitem.top === 1">mdi-menu-right-outline</v-icon>
            {{ sitem.name }}
            </span>
          </td>
        </tr>
        </tbody>
      </v-table>
    </v-col>
  </v-row>

</template>

<style scoped>
.v-row{
  border-right: solid thin grey;
  border-bottom: solid thin grey;
}

.v-col-sm-4 {
  border-left: solid thin grey;
}

.v-col-md-2 {
  border-left: solid thin grey;
}
 .v-col-12 {
  border-left: solid thin grey;
}
.v-table .v-table__wrapper > table > tbody > tr:not(:last-child) > td, .v-table .v-table__wrapper > table > tbody > tr:not(:last-child) > th {
  border-bottom: 0;
}
.v-table--density-compact > .v-table__wrapper > table > tbody > tr > td {
  height: 25px;
  padding: 0 5px
}

</style>
