<template>
  <div class="picbox">
    <ul>
     <li class="reveal-top" data-scroll-reveal="enter bottom over 1s">

        <a href="/"><i><img src="../../assets/imgs/b01.jpg"></i>
          <div class="picinfo">
            <h3>个人博客模板《繁花》</h3>
            <span>好咖啡要和朋友一起品尝，好“模板”也要和同样喜欢它的人一起分享。</span>
          </div>
        </a>
      </li>
       <li class="reveal-top" data-scroll-reveal="enter bottom over 1s">
        <a href="/"><i><img src="../../assets/imgs/b02.jpg"></i>
          <div class="picinfo">
            <h3>个人博客模板《繁花》</h3>
            <span>好咖啡要和朋友一起品尝，好“模板”也要和同样喜欢它的人一起分享。</span>
          </div>
        </a>
      </li>
      <li class="reveal-top" data-scroll-reveal="enter bottom over 1s">
        <a href="/"><i><img src="../../assets/imgs/b03.jpg"></i>
          <div class="picinfo">
            <h3>个人博客模板《繁花》</h3>
            <span>好咖啡要和朋友一起品尝，好“模板”也要和同样喜欢它的人一起分享。</span>
          </div>
        </a>
      </li>
       <li class="reveal-top" data-scroll-reveal="enter bottom over 1s">
        <a href="/"><i><img src="../../assets/imgs/b05.jpg"></i>
          <div class="picinfo">
            <h3>个人博客模板《繁花》</h3>
            <span>好咖啡要和朋友一起品尝，好“模板”也要和同样喜欢它的人一起分享。</span>
          </div>
        </a>
      </li>
       <li class="reveal-top" data-scroll-reveal="enter bottom over 1s">
        <a href="/"><i><img src="../../assets/imgs/b04.jpg"></i>
          <div class="picinfo">
            <h3>个人博客模板《繁花》</h3>
            <span>好咖啡要和朋友一起品尝，好“模板”也要和同样喜欢它的人一起分享。</span>
          </div>
        </a>
      </li>
    </ul>
   <ul>
     <li class="reveal-top" data-scroll-reveal="enter bottom over 1s">
        <a href="/"><i><img src="../../assets/imgs/b05.jpg"></i>
          <div class="picinfo">
            <h3>个人博客模板《繁花》</h3>
            <span>好咖啡要和朋友一起品尝，好“模板”也要和同样喜欢它的人一起分享。</span>
          </div>
        </a>
      </li>
       <li class="reveal-top" data-scroll-reveal="enter bottom over 1s">
        <a href="/"><i><img src="../../assets/imgs/b02.jpg"></i>
          <div class="picinfo">
            <h3>个人博客模板《繁花》</h3>
            <span>好咖啡要和朋友一起品尝，好“模板”也要和同样喜欢它的人一起分享。</span>
          </div>
        </a>
      </li>
      <li class="reveal-top" data-scroll-reveal="enter bottom over 1s">
        <a href="/"><i><img src="../../assets/imgs/b03.jpg"></i>
          <div class="picinfo">
            <h3>个人博客模板《繁花》</h3>
            <span>好咖啡要和朋友一起品尝，好“模板”也要和同样喜欢它的人一起分享。</span>
          </div>
        </a>
      </li>
       <li class="reveal-top" data-scroll-reveal="enter bottom over 1s">
        <a href="/"><i><img src="../../assets/imgs/b05.jpg"></i>
          <div class="picinfo">
            <h3>个人博客模板《繁花》</h3>
            <span>好咖啡要和朋友一起品尝，好“模板”也要和同样喜欢它的人一起分享。</span>
          </div>
        </a>
      </li>
       <li class="reveal-top" data-scroll-reveal="enter bottom over 1s">
        <a href="/"><i><img src="../../assets/imgs/b04.jpg"></i>
          <div class="picinfo">
            <h3>个人博客模板《繁花》</h3>
            <span>好咖啡要和朋友一起品尝，好“模板”也要和同样喜欢它的人一起分享。</span>
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>
<script>
import scrollReveal from "scrollreveal";

export default {
    name: "",
    data() {
        return {
            scrollReveal: scrollReveal()
        };
    },
    mounted() {
        this.scrollReveal.reveal(".reveal-top", {
            // 动画的时长
            duration: 1000,
            // 延迟时间
            delay: 500,
            // 动画开始的位置，'bottom', 'left', 'top', 'right'
            origin: "bottom",
            // 回滚的时候是否再次触发动画
            reset: true,
            // 在移动端是否使用动画
            mobile: false,
            // 滚动的距离，单位可以用%，rem等
            distance: "200px",
            // 其他可用的动画效果
            opacity: 0.001,
            easing: "linear",
            scale: 0.9
        });
    }
};
</script>
<style lang="less" scoped>
.picbox {
    width: 100%;
    overflow: hidden;
    display:block;
    ul {
        overflow: hidden;
        width: 24%;
        float: left;
        margin-right: 10px;
        display: block;
        li {
            -webkit-transform: translatey(0);
            transform: translatey(0);
            opacity: 1;
            -webkit-transition: -webkit-transform 1s ease-in-out 0s,
                opacity 1s ease-in-out 0s;
            transition: transform 1s ease-in-out 0s, opacity 1s ease-in-out 0s;
            -webkit-perspective: 1000;
            -webkit-backface-visibility: hidden;
            list-style: none;
            a {
                text-decoration: none;
                color: #555;
                i {
                    margin: 10px;
                    height: auto;
                    overflow: hidden;
                    display: block;
                    img {
                        width: 100%;
                    }
                }
            }
        }
    }
}
</style>
