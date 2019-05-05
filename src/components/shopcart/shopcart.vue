<template>
  <div>
    <div class="shopcart">
      <div class="content">
        <div class="content-left">
          <div class="logo-wrapper">
            <div class="logo">
              <i class="icon-shopping_cart"></i>
            </div>
          </div>
          <div class="price">0元</div>
          <div class="desc">另需配送费¥{{deliveryPrice}}</div>
        </div>
        <div class="content-right">
          <div class="pay">
            ¥{{minPrice}}起送
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script type="text/ecmascript-6">
export default {
  props: {
    deliveryPrice: {
      type: Number,
      default: 0
    },
    minPrice: {
      type: Number,
      default: 0
    }
  },
  data() {
    return {};
  },
  components: {}
};
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import "../../common/stylus/mixin.styl"
  .shopcart
    position: fixed
    left: 0
    bottom: 0
    z-index: 50
    width: 100%
    height: 48px
    background: #000
    .content
      display: flex
      background: #141d27
      font-size: 0
      .content-left
        flex: 1
        .logo-wrapper
          display: inline-block
          vertical-align: top
          position: relative
          top: -10px
          margin: 0 12px
          padding: 6px
          width: 56px
          height: 56px
          box-sizing: border-box      // ie盒模型，高度宽度包括了外层的padding
          border-radius: 50%           // 常用技巧50%就是圆
          background: #141d27      //  否则是透明的，技术冒出也看不到。
          .logo
            width: 100%       // 撑满父元素即可。
            height: 100%
            border-radius: 50%
            text-align: center
            background: #2b343c
            .icon-shopping_cart
              line-height: 44px
              font-size: 24px
              color: #80858a

        .price
          display: inline-block
          vertical-align: top
          margin-top: 12px
          line-height: 24px
          padding-right: 12px
          box-sizing: border-box
          border-right: 1px solid rgba(255,255,255,0.1)
          font-size: 16px
          font-weight: 700px
          color: rgba(255,255,255,0.4)
        .desc
          display: inline-block
          vertical-align: top
          margin: 12px 0 0 12px
          line-height: 24px
          color: rgba(255,255,255,0.4)
          font-size: 10px

      .content-right
        flex: 0 0 105px
        width: 105px
        .pay
          height: 48px
          line-height: 48px
          text-align: center
          font-size: 12px
          color: rgba(255,255,255,0.4)
          font-weight: 700
          background: #2b333b



</style>
