<template>
  <div class="home">
    <div class="container-1">
      <div class="circles">
        <div
          class="my-element"
          @click="toggleCircle1"
          :class="{
            'my-circle': !circle1.expanded,
            'my-square': circle1.expanded,
            'container-center': circle1.expanded,
          }"
        >
          <img
            class="logo-center"
            :class="{
              'hide-element': circle1.expanded,
            }"
            src="@/assets/moon.svg"
            alt=""
          />
          <p
            class="text-container"
            :class="{
              'hide-element': !circle1.expanded,
              'show-text': circle1.expanded,
            }"
          >
            Here we go 1
          </p>
        </div>
        <!-- End Circle -->
        <div
          class="my-element"
          @click="toggleCircle2"
          :class="{
            'my-circle': !circle2.expanded,
            'my-square': circle2.expanded,
            'container-center': circle2.expanded,
          }"
        >
          <p
            class="text-container"
            :class="{
              'hide-element': !circle2.expanded,
              'show-text': circle2.expanded,
            }"
          >
            Here we go 2
          </p>
        </div>
        <!-- End Circle -->
        <div
          class="my-element"
          @click="toggleCircle3"
          :class="{
            'my-circle': !circle3.expanded,
            'my-square': circle3.expanded,
            'container-center': circle3.expanded,
          }"
        >
          <p
            class="text-container"
            :class="{
              'hide-element': !circle3.expanded,
              'show-text': circle3.expanded,
            }"
          >
            Here we go 3
          </p>
        </div>
        <!-- End Circle -->
        <div
          class="my-element"
          @click="toggleCircle4"
          :class="{
            'my-circle': !circle4.expanded,
            'my-square': circle4.expanded,
            'container-center': circle4.expanded,
          }"
        >
          <p
            class="text-container"
            :class="{
              'hide-element': !circle4.expanded,
              'show-text': circle4.expanded,
            }"
          >
            Here we go 4
          </p>
        </div>
        <!-- End Circle -->
      </div>
      <!-- End Circles -->
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      circle1: {
        expanded: false,
      },
      circle2: {
        expanded: false,
      },
      circle3: {
        expanded: false,
      },
      circle4: {
        expanded: false,
      },
    };
  },
  methods: {
    toggleCircle1() {
      if (this.circle1.expanded === false) {
        this.circle1.expanded = true;
      } else {
        this.circle1.expanded = false;
      }
      this.circle2.expanded = false;
      this.circle3.expanded = false;
      this.circle4.expanded = false;
    },
    toggleCircle2() {
      if (this.circle2.expanded === false) {
        this.circle2.expanded = true;
      } else {
        this.circle2.expanded = false;
      }
      this.circle1.expanded = false;
      this.circle3.expanded = false;
      this.circle4.expanded = false;
    },
    toggleCircle3() {
      if (this.circle3.expanded === false) {
        this.circle3.expanded = true;
      } else {
        this.circle3.expanded = false;
      }
      this.circle1.expanded = false;
      this.circle2.expanded = false;
      this.circle4.expanded = false;
    },
    toggleCircle4() {
      if (this.circle4.expanded === false) {
        this.circle4.expanded = true;
      } else {
        this.circle4.expanded = false;
      }
      this.circle1.expanded = false;
      this.circle2.expanded = false;
      this.circle3.expanded = false;
    },
  },
};
</script>

<style lang="scss" scoped>
.container-1 {
  margin-top: 90px;
  margin-left: 90px;
  display: flex;
}

.container-center {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 80vh;
}

.circles {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  align-items: space-evenly;
}

.my-element {
  background: #f2f2f2;
  box-shadow: 0px -6px 10px rgba(255, 255, 255, 1),
    0px 4px 15px rgba(0, 0, 0, 0.15);
  cursor: pointer;
  position: relative;
  text-align: center;
  align-content: center;
  align-items: center;
}

.my-circle {
  width: 92px;
  height: 92px;
  border-radius: 50px;

  box-shadow: 0px -6px 10px rgba(255, 255, 255, 1),
    0px 4px 15px rgba(0, 0, 0, 0.15);
}

.my-square {
  width: 500px;
  height: 500px;
  border-radius: 18px;
}

.text-container {
  opacity: 0;
  -webkit-animation: fadein 2s; /* Safari, Chrome and Opera > 12.1 */
  -moz-animation: fadein 2s; /* Firefox < 16 */
  -ms-animation: fadein 2s; /* Internet Explorer */
  -o-animation: fadein 2s; /* Opera < 12.1 */
  animation: fadein 2s;
  animation-fill-mode: forwards;
}

@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.show-text {
  display: block;
}

.hide-element {
  display: none;
}

.logo-center {
  margin-top: 36%;
}
</style>