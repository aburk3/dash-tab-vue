<template>
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
        <font-awesome-icon
          :icon="gemIcon"
          size="3x"
          :style="{ color: 'black' }"
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
</template>

<script>
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { faGem } from "@fortawesome/free-solid-svg-icons";

export default {
  name: "SkillSet",
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
      gemIcon: faGem,
    };
  },
  components: {
    FontAwesomeIcon,
  },
  methods: {
    closeAllCircles() {
      this.circle1.expanded = false;
      this.circle2.expanded = false;
      this.circle3.expanded = false;
      this.circle4.expanded = false;
    },
    toggleCircle(circle, state) {
      this.closeAllCircles();
      state == true ? (circle.expanded = false) : (circle.expanded = true);
    },
    toggleCircle1() {
      let state = this.circle1.expanded;
      this.toggleCircle(this.circle1, state);
    },
    toggleCircle2() {
      let state = this.circle2.expanded;
      this.toggleCircle(this.circle2, state);
    },
    toggleCircle3() {
      let state = this.circle3.expanded;
      this.toggleCircle(this.circle3, state);
    },
    toggleCircle4() {
      let state = this.circle4.expanded;
      this.toggleCircle(this.circle4, state);
    },
  },
};
</script>

<style lang="scss" scoped>
.container-1 {
  margin-top: 90px;
  margin-left: 24%;
  display: flex;
  position: absolute;
  z-index: 5;
}

.container-center {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 25vh;
}

.circles {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  align-items: space-evenly;
}

.my-element {
  background: #f2f2f2;
  box-shadow: -3px -3px 3px 0 rgba(255, 255, 255, 0.04),
    2px 2px 5px 0 rgba(0, 0, 0, 2);
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

  box-shadow: -3px -3px 3px 0 rgba(255, 255, 255, 0.04),
    2px 2px 5px 0 rgba(0, 0, 0, 2);
}

.my-square {
  width: 200px;
  height: 200px;
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