<template>
    <div>
          <div class="title">
            <slot name="title"></slot>
            <span class="btn" @click="isShow = !isShow">
              {{ isShow ? '收起' : '展开' }}
            </span>
          </div>
          <div class="container" v-show="isShow">
              <slot name="container" tit="hello"  :list="arr">默认内容</slot>
          </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                isShow: false,
                arr:[
                  {  
                    id:1,
                    name:"寒雨连江夜入吴,",
                    },
                      {  
                    id:2,
                    name:"平明送客楚山孤。",
                    },
                      {  
                    id:3,
                    name:"洛阳亲友如相问，",
                    },
                      {  
                    id:4,
                    name:"一片冰心在玉壶。",
                    }
                ],
            }
        },
    }
</script>

<style scoped>

</style>