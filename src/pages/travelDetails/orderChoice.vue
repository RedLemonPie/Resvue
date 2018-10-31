<template>
  <div>
    <section class="topBuyItem" data-stat-display="2" data-stat-area="3_1">
      <a class="hd" href="#buyPop">
        选择：套餐类型/日期/人群
        <div class="term">班期：10/30-12/19</div>
      </a>
      <div class="bd"><a class="booking" href="#buyPop" data-brief-date="2018-10-30">
          <div class="date">10-30 周二</div>
          <div class="price">￥16280</div>
        </a><a class="booking" href="#buyPop" data-brief-date="2018-10-31">
          <div class="date">10-31 周三</div>
          <div class="price">￥15999</div>
        </a><a class="booking" href="#buyPop" data-brief-date="2018-11-01">
          <div class="date">11-01 周四</div>
          <div class="price">￥15499</div>
        </a><a class="booking" href="#buyPop" data-brief-date="2018-11-02">
          <div class="date">11-02 周五</div>
          <div class="price">￥15699</div>
        </a><a class="booking" href="#buyPop" data-brief-date="2018-11-03">
          <div class="date">11-03 周六</div>
          <div class="price">￥15499</div>
        </a><a class="booking" href="#buyPop" data-brief-date="2018-11-04">
          <div class="date">11-04 周日</div>
          <div class="price">￥15499</div>
        </a><a class="booking" href="#buyPop" data-brief-date="2018-11-05">
          <div class="date">11-05 周一</div>
          <div class="price">￥15150</div>
        </a><a class="booking" href="#buyPop" data-brief-date="2018-11-06">
          <div class="date">11-06 周二</div>
          <div class="price">￥15500</div>
        </a></div>
      <a href="#buyPop" class="more">更多<br>班期</a>

      <!-- block:remind -->
      <div class="remind-box" data-stat-area="3_3">
        <i class="icon-remind"></i>
        <p>此产品需要二次确认，商家将在18个工作小时内（工作日9:00-18:00）核实是否有位!</p>
      </div>

    </section>
  </div>
</template>

<script>
import { Divider, Card } from "vux";

export default {
  components: {
    Divider
  },
  data() {
    return {
      details: {
        name:
          "我没有名字我就是个内容,我没有名字我就是个内容,我没有名字我就是个内容,我没有名字我就是个内容我没有名字我就是个内容",
        tags: ["住不下去", "凡不能吃", "谁不能喝", "厕所不能上"],
        symbal: "$",
        low_price: 2000,
        high_price: 4000,
        sold: 1000
      }
    };
  }
};
</script>

<style scoped lang="less">
@import "~vux/src/styles/1px.less";

a {
  text-decoration: none;
  color: #474747;
}

.topBuyItem {
  background-color: #fff;
  margin-bottom: 0.2666666667rem;
  position: relative;
  overflow: hidden;
  .hd {
    display: block;
    padding: 0.4rem 0.2666666667rem;
    font-size: 0.4rem;
    position: relative;
    line-height: 1em;
    .term {
      position: absolute;
      right: 0.2666666667rem;
      font-size: 0.32rem;
      top: 0.4rem;
      padding: 0 0.4rem 0 0;
    }
  }
  .bd {
    overflow: auto;
    -webkit-overflow-scrolling: touch;
    position: relative;
    font-size: 0;
    padding: 0 1.4666666667rem 0.4rem 0.2666666667rem;
    white-space: nowrap;
    a {
      display: inline-block;
      position: relative;
      text-align: center;
      font-size: 0.32rem;
      margin-right: 0.2666666667rem;
      .date {
        padding: 0.3466666667rem 0.2666666667rem 0.1333333333rem;
        line-height: 1em;
      }
      .topBuyItem .bd .price {
        padding: 0 0.2666666667rem 0.2666666667rem;
        font-weight: 600;
      }   
    }
  }
}
</style>