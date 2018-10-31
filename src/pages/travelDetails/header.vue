<template>
	<div>
		<card>
			<div slot="content" class="itemInfo">
				<h1>
					<!-- block:top:title -->
					<span class="shop-icon">店铺</span><span>{{details.name}}</span>
				</h1>
				<div class="tags">
					<span v-for="tag in details.tags" :key="tag">
						{{tag}}
					</span>
				</div>

				<div class="price">
					<em>{{details.symbal}}</em>
					<strong>{{details.low_price}}~{{details.high_price}}</strong>
					<a href="javascript:void(0);" class="explan" data-content="本产品可售日期范围内的最低价和最高价。其中最低价库存为：<br>7天 5晚 上海新航（更多航班天数详询客服） 1晚马累+2晚沙滩套房+2晚豪华水上别墅 2018-11-05">价格说明</a>
					<div class="sold">月售{{details.sold}}</div>
				</div>

				<Goldcard></Goldcard>

				<a href="javascript:void(0);" class="extra" style="background-color: rgb(255, 255, 255);" data-stat-area="2_5" data-promotion-list="">
					<ul>
						<li>
							<div class="t"><span>立减</span></div>
							10.8-10.31期间，限时下单立减200元！
						</li>
					</ul>
				</a>
			</div>
		</card>
	</div>
</template>

<script>
import { Divider, Card } from "vux";
import Goldcard from "./goldcard";

export default {
  components: {
    Card,
    Divider,
    Goldcard
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
.itemInfo {
  padding: 0.2666666667rem 0.2666666667rem 0;
  background-color: #fff;
  position: relative;
  margin-bottom: 0.2666666667rem;
  overflow: hidden;
  .shop-icon {
    background: -webkit-gradient(
      linear,
      right top,
      left top,
      from(#5991ff),
      to(#80aaff)
    );
    background: linear-gradient(-90deg, #5991ff, #80aaff);
    font-size: 0.2933333333rem;
    color: #fff;
    display: inline-block;
    font-weight: normal;
    margin-right: 5px;
    line-height: 1.2;
    padding: 0.0666666667rem 0.1333333333rem;
    border-radius: 0.0533333333rem;
    vertical-align: middle;
    margin-top: -1px;
    font-weight: 600;
  }
  h1 {
    font-size: 0.4266666667rem;
    line-height: 1.4em;
  }
  span {
    font-size: 0.4266666667rem;
    padding: 0 0.2666666667rem;
  }
  .tags {
    width: 20rem;
    max-height: 0.3466666667rem;
    -webkit-transform: scale(0.5);
    transform: scale(0.5);
    -webkit-transform-origin: 0 0;
    transform-origin: 0 0;
    span {
      font-size: 0.5333333333rem;
      color: #696969;
      line-height: 0.6933333333rem;
      border: 1px solid #e5e5e5;
      border-radius: 0.1066666667rem;
      margin: 0 0.4333333333rem 0.2133333333rem 0;
      padding: 0 0.1066666667rem;
      display: inline-block;
    }
  }
  .price {
    font-size: 0;
    color: #ff4a26;
    padding: 0.4rem 0.2666666667rem 0.2666666667rem 0;
    margin: 0.2666666667rem 0;
    position: relative;
    em {
      font-size: 0.533333rem;
      // line-height: 0em;
      // vertical-align: top;
      font-style: normal;
			font-weight: bold;
    }
    strong {
      font-size: 0.5333333333rem;
    }
    a {
      font-size: 0.32rem;
      color: #30a2f3;
      margin-left: 0.2rem;
    }
    .sold {
      font-size: 0.32rem;
      color: #767676;
      line-height: 0.4rem;
      position: absolute;
      right: 0.2666666667rem;
      bottom: 0.3666666667rem;
    }
  }
  .extra {
    display: block;
    line-height: 0.5866666667rem;
    font-size: 0.32rem;
    margin: 0;
    padding: 0.3666666667rem 0 0 ;
    position: relative;
    ul {
      list-style: none;
      li {
        padding-right: 0.2933333333rem;
      }
    }
    .t {
      display: inline-block;
      width: 0.7933333333rem;
      height: 0.3333333333rem;
      overflow: hidden;
      vertical-align: middle;
      margin: 0 0.1066666667rem 0.0533333333rem 0;
      span {
        display: inline-block;
        height: 0.5866666667rem;
        white-space: nowrap;
        line-height: 0.5866666667rem;
        text-align: center;
        border: 1px solid;
        color: #ff4a26;
        font-size: 0.48rem;
        -webkit-transform: scale(0.5);
        transform: scale(0.5);
        -webkit-transform-origin: 0 0;
        transform-origin: 0 0;
      }
    }
  }
}

.card-demo-flex {
  display: flex;
}
.card-demo-content01 {
  padding: 10px 0;
}
.card-padding {
  padding: 15px;
}
.card-demo-flex > div {
  flex: 1;
  text-align: center;
  font-size: 12px;
}
.card-demo-flex span {
  color: #f74c31;
}
</style>