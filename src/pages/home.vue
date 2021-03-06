<template>
  <div class="ctn-block home-page">
    <div class="banner text-center">
      <h1 class="home-title"><span class="apache">Apache</span> <span class="linkis">Linkis</span> <span class="badge">Incubating</span></h1>
      <p class="home-desc">{{$t('message.home.banner.slogan')}}</p>
      <div class="botton-row center">
        <a href="/" class="corner-botton black">Get Started</a>
        <a href="/" class="corner-botton white">GitHub</a>
      </div>
    </div>
    <h1 class="home-block-title text-center">Computation Governance Concept</h1>
    <div class="concept home-block">
      <div class="concept-item">
        <h3 class="concept-title">Before</h3>
        <p class="home-paragraph">Each upper application directly connects to and accesses various underlying engines in a tightly coupled way, which makes big data platform a complex network architecture.</p>
        <!-- <img src="" alt="before" class="concept-image"> -->
      </div>
      <div class="concept-item">
        <h3 class="concept-title">After</h3>
        <p class="home-paragraph">Build a common layer of "computation middleware" between the numerous upper-layer applications and the countless underlying engines to resolve these complex connection problems in a standardized reusable way</p>
        <!-- <img src="" alt="after" class="concept-image"> -->
      </div>
    </div>
    <div class="description home-block">
      <div class="description-content">
        <h1 class="home-block-title">Description</h1>
        <p class="home-paragraph">Linkis provides standardized interfaces (REST, JDBC, WebSocket etc.) to easily connect to various underlying engines (Spark, Presto, Flink, etc.), and acts as a proxy between the upper applications layer and underlying engines layer. </p>
        <p class="home-paragraph">Linkis is able to facilitate the connectivity, governance and orchestration capabilities of different kind of engines like OLAP, OLTP (developing), Streaming, and handle all these "computation governance" affairs in a standardized reusable way.</p>
        <div class="botton-row">
          <a href="/" class="corner-botton blue">Learn More</a>
        </div>
      </div>
      <!-- <img src="" alt="description" class="description-image"> -->
    </div>
    <h1 class="home-block-title text-center">Core Features</h1>
    <div class="features home-block">
      <div class="feature-item">
        <div class="item-content">
          <h3 class="item-title">Connectivity</h3>
          <p class="item-desc">Simplify the operation environment; decouple the upper and lower layers, which make the upper layer insensitive when bottom layers changed</p>
        </div>
      </div>
      <div class="feature-item">
        <div class="item-content">
          <h3 class="item-title">Scalability</h3>
          <p class="item-desc">Distributed microservice architecture with great scalability and extensibility; quickly integrate with the new underlying engine</p>
        </div>
      </div>
      <div class="feature-item">
        <div class="item-content">
          <h3 class="item-title">Controllability</h3>
          <p class="item-desc">Converge engine entrance, unify identity verification, high-risk prevention and control, audit records; label-based multi-level refined resource control and recovery capabilities</p>
        </div>
      </div>
      <div class="feature-item">
        <div class="item-content">
          <h3 class="item-title">Orchestration</h3>
          <p class="item-desc">Computing strategy design based on active-active, mixed computing, transcation Orchestrator Service</p>
        </div>
      </div>
      <div class="feature-item">
        <div class="item-content">
          <h3 class="item-title">Reusability</h3>
          <p class="item-desc">Highly reduced the back-end development workload of upper-level applications development; Swiftly and efficiently build a data platform tool suite based on Linkis</p>
        </div>
      </div>
    </div>
    <h1 class="home-block-title text-center">Showcase</h1>
    <div class="show-case home-block">
      <div class="case-item"></div>
      <div class="case-item"></div>
      <div class="case-item"></div>
      <div class="case-item"></div>
      <div class="case-item"></div>
      <div class="case-item"></div>
      <div class="case-item"></div>
    </div>
  </div>
</template>
<style lang="less" scoped>
  @import url('/src/style/variable.less');
  @import url('/src/style/base.less');

  .home-page {
    .home-block-title{
      margin-bottom: 20px;
      font-size: 32px;
      line-height: 46px;
    }
    .home-block{
      padding: 20px 0 88px;
      .home-paragraph{
        font-size: 18px;
        color: #4A4A4A;
        line-height: 26px;
        font-weight: 400;
        margin-bottom: 16px;
      }
    }
    .description{
      display: flex;
      align-items: center;
      .description-content{
        flex: 1;
      }
      .description-image{
        margin-left: 40px;
      }
    }

    .concept{
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      grid-column-gap: 20px;
      .concept-item{
        padding: 30px 20px;
        border: 1px dashed #979797;
        border-radius: 10px;
        .concept-title{
          font-size: 24px;
          line-height: 34px;
          margin-bottom: 16px;
          color: @enhance-color;
        }
        .concept-image{
          width: 100%;
        }
      }
    }
    .show-case{
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      grid-row-gap: 20px;
      grid-column-gap: 20px;
      .case-item{
        height: 88px;
        background: #FFFFFF;
        box-shadow: 0 1px 20px 0 rgba(15,18,34,0.10);
        border-radius: 8px;
      }
    }
    .features{
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      grid-column-gap: 20px;
      .feature-item{
        height: 370px;
        background: #FFFFFF;
        box-shadow: 0 0 16px 0 rgba(211,211,211,0.50);
        border-radius: 10px;
        padding-top: 100px;
        background-repeat: no-repeat;
        background-size: 100%;
        background-position: center top;
        .item-content{
          padding: 30px 20px;
          text-align: left;
          .item-title{
            margin-bottom: 20px;
            color: #393939;
            line-height: 26px;
            font-size: 18px;
            font-weight: 500;
          }
          .item-desc{
            color: #666666;
            line-height: 22px;
            font-weight: 400;
          }
        }
      }
    }
    .banner {
      padding: 168px 0;
      .home-title {
        margin-bottom: 20px;
        font-size: 60px;
        line-height: 84px;

        .apache {
          color: @enhance-color;
        }

        .linkis {
          color: #1A529C;
        }

        .badge {
          font-size: 24px;
          font-weight: 400;
        }
      }

      .home-desc {
        margin-bottom: 80px;
        font-size: 24px;
        color: @enhance-color;
        text-align: center;
        line-height: 26px;
        font-weight: 400;
      }
    }

    .botton-row{
      display: flex;
      &.center{
        justify-content: center;
      }
      .corner-botton{
        margin-right: 22px;
        padding: 0 40px;
        height: 46px;
        line-height: 46px;
        border-radius: 25px;
        &:last-child{
          margin-right: 0;
        }
        &.black{
          color: #fff;
          background: @enhance-color;
          border: 1px solid  @enhance-color;
        }
        &.white{
          color: @enhance-color;
          background: #fff;
          border: 1px solid @enhance-color;
        }
        &.blue{
          color: #1A529C;
          border: 1px solid #1A529C;
        }
      }
    }
  }
</style>