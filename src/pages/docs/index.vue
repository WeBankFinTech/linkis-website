<template>
  <div class="ctn-block reading-area">
    <main class="main-content">
      <router-view></router-view>
    </main>
    <div class="side-bar">
      <router-link :to="doc.link" class="bar-item" v-for="(doc,index) in docs" :key="index">{{doc.title}}
        <router-link :to="children.link" class="bar-item" v-for="(children,cindex) in doc.children" :key="cindex">{{children.title}}
        </router-link>
      </router-link>
    </div>
  </div>
</template>
<style lang="less">
  .reading-area {
    display: flex;
    padding: 60px 0;
    min-height: 600px;

    .main-content {
      width: 900px;
      padding: 30px;
    }

    .side-bar {
      flex: 1;
      padding: 18px 0;
      border-left: 1px solid #eaecef;

      .bar-item {
        display: block;
        padding: 5px 18px;
        color: #4A4A4A;
      }
    }
  }
</style>
<script setup>
  const docs = [{
    title: '部署文档',
    link: '/docs/deploy/main',
    children: [{
      title: '快速部署 Linkis1.0',
      link: '/docs/deploy/linkis',
    }, {
      title: '快速安装 EngineConnPlugin 引擎插件',
      link: '/docs/deploy/engins',
    }, {
      title: 'Linkis1.0 分布式部署手册',
      link: '/docs/deploy/distributed',
    }, {
      title: 'Linkis1.0 安装包目录层级结构详解',
      link: '/docs/deploy/structure',
    }]
  }]
</script>