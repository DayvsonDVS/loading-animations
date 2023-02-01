<template>
  <div class="index">
    <section>
      <div class="loader">
        <span style="--i: 1" />
        <span style="--i: 2" />
        <span style="--i: 3" />
        <span style="--i: 4" />
        <span style="--i: 5" />
        <span style="--i: 6" />
        <span style="--i: 7" />
        <span style="--i: 8" />
        <span style="--i: 9" />
        <span style="--i: 10" />
        <span style="--i: 11" />
        <span style="--i: 12" />
        <span style="--i: 13" />
        <span style="--i: 14" />
        <span style="--i: 15" />
        <span style="--i: 16" />
        <span style="--i: 17" />
        <span style="--i: 18" />
        <span style="--i: 19" />
        <span style="--i: 20" />
      </div>
    </section>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.index {
  section {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: #042104;
    animation: animateBg 10s linear infinite;
    @keyframes animateBg {
      0% {
        filter: hue-rotate(0deg);
      }
      100% {
        filter: hue-rotate(360deg);
      }
    }
    .loader {
      position: relative;
      width: 120px;
      height: 120px;
      span {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        transform: rotate(calc(18deg * var(--i)));
        &::before {
          content: '';
          position: absolute;
          top: 0;
          left: 0;
          width: 15px;
          height: 15px;
          border-radius: 50%;
          background: #00ff0a;
          box-shadow: 0 0 10px #00ff0a, 0 0 20px #00ff0a, 0 0 40px #00ff0a,
            0 0 60px #00ff0a, 0 0 80px #00ff0a;
          animation: animate 2s linear infinite;
          animation-delay: calc(0.1s * var(--i));

          @keyframes animate {
            0% {
              transform: scale(1);
            }
            80%,
            100% {
              transform: scale(0);
            }
          }
        }
      }
    }
  }
}
</style>
