<template lang="pug">
main.responsive

  button
    span Date
    menu.round.no-wrap
      datePicker
  .row
    a(@click="updateTheme()")
      i.large palette
    .max
      h5 Test your changes here
      div Click on icon to change theme
  dialog.round.large-padding#default(data-ui="#default")
    h5 Default dialog
    nav.right-align
      button.border Cancel
      button Confirm

  dialog.left#left(data-ui="#left")
    h5 Left dialog
    nav.right-align
      button.border Cancel
      button Confirm

  dialog.top#top(data-ui="#top")
    h5 Top dialog
    nav.right-align
      button.border Cancel
      button Confirm

  dialog.right#right(data-ui="#right")
    h5 Right dialog
    nav.right-align
      button.border Cancel
      button Confirm

  dialog.bottom#bottom(data-ui="#bottom")
    h5 Bottom dialog
    nav.right-align
      button.border Cancel
      button Confirm

  .field.label.border
    input
    label.front
      span Label
      a
        i info
        .tooltip Tooltip
      a
        img.circle(:src="'/favicon.png'")
        .tooltip Tooltip
      a
        svg(viewBox="0 0 24 24")
          path(d="M12,2A10,10 0 0,0 2,12A10,10 0 0,0 12,22A10,10 0 0,0 22,12A10,10 0 0,0 12,2M7.07,18.28C7.5,17.38 10.12,16.5 12,16.5C13.88,16.5 16.5,17.38 16.93,18.28C15.57,19.36 13.86,20 12,20C10.14,20 8.43,19.36 7.07,18.28M18.36,16.83C16.93,15.09 13.46,14.5 12,14.5C10.54,14.5 7.07,15.09 5.64,16.83C4.62,15.5 4,13.82 4,12C4,7.59 7.59,4 12,4C16.41,4 20,7.59 20,12C20,13.82 19.38,15.5 18.36,16.83M12,6C10.06,6 8.5,7.56 8.5,9.5C8.5,11.44 10.06,13 12,13C13.94,13 15.5,11.44 15.5,9.5C15.5,7.56 13.94,6 12,6M12,11A1.5,1.5 0 0,1 10.5,9.5A1.5,1.5 0 0,1 12,8A1.5,1.5 0 0,1 13.5,9.5A1.5,1.5 0 0,1 12,11Z")
        .tooltip Tooltip

    span.helper Helper

  nav
    button(data-ui="#default") Default
    button(data-ui="#left") Left
    button(data-ui="#top") Top
    button(data-ui="#right") Right
    button(data-ui="#bottom") Bottom
  h5 Binding
  .row
    .field.label.border
      input(v-model="number")
      label Input
    .field.label.border
      input(v-model="number")
      label Test
    label.slider.large.min
      input(type="range", v-model="number")
      span
    progress(:value="number", max="100")
    progress
  .row
    .field.label.border.max
      select(v-model="select")
        option
        option(value="1") Item 1
        option(value="2") Item 2
        option(value="3") Item 3
      label Test
    .field.border
      select(v-model="select")
        option
        option(value="1") Item 1
        option(value="2") Item 2
        option(value="3") Item 3
  h5 With pure CSS
  nav
    button(@click="domain.updateSize('#with-pure-css .field', 'small')") small
    button(@click="domain.updateSize('#with-pure-css .field', '')") medium
    button(@click="domain.updateSize('#with-pure-css .field', 'large')") large
    button(@click="domain.updateSize('#with-pure-css .field', 'extra')") extra
  .space
  #with-pure-css.grid
    .s12.m6
      .field.label.fill
        input(placeholder=" ")
        label Label
        span.helper Helper
    .s12.m6
      .field.label.fill.prefix
        i home
        input(placeholder=" ", disabled, value="100")
        label Label
        span.helper Helper
    .s12.m6
      .field.label.fill.round
        input(placeholder=" ")
        label Label
        span.helper Helper
    .s12.m6
      .field.label.fill.prefix.round
        i home
        input(placeholder=" ")
        label Label
        span.helper Helper
    .s12.m6
      .field.label.border
        input(placeholder=" ")
        label Label
        span.helper Helper
    .s12.m6
      .field.label.border.prefix
        i home
        input(placeholder=" ", disabled, value="100")
        label Label
        span.helper Helper
    .s12.m6
      .field.label.border.round
        input(placeholder=" ")
        label Label
        span.helper Helper
    .s12.m6
      .field.label.border.prefix.round
        i home
        input(placeholder=" ")
        label Label
        span.helper
          span Helper
          i.tiny info
          .tooltip.bottom Testando tooltip
  h5 With row
  .grid
    .s4
      .field.label.border
        input
        label Label
        span.helper Helper
    .s4
      .field.label.border
        input
        label Label
        span.helper Helper
    .s4
      .field.label.border
        input
        label Label
        span.helper Helper
    .s4
      .field.label.border
        input
        label Label
        span.helper Helper
    .s4
      .field.label.border
        input
        label Label
        span.helper Helper
    .s4
      .field.label.border
        input
        label Label
        span.helper Helper
    .s6
      .field.label.border
        input
        label Label
        span.helper Helper
      .field.label.border
        input
        label Label
        span.helper Helper
      .field.label.border
        input
        label Label
        span.helper Helper
    .s6
      .field.label.border
        input
        label Label
        span.helper Helper
      .field.label.border
        input
        label Label
        span.helper Helper
      .field.label.border
        input
        label Label
        span.helper Helper
    .s12
      .field.label.border
        input
        label Label
        span.helper Helper
      .field.label.border
        input
        label Label
        span.helper Helper
      .field.border.label.border
        input
        label Label
        span.helper Helper
    .s12.m6
      .field.border.label
        input
        label Label
        span.helper Helper
    .s12.m6
      .field.middle-align
        label.slider
          input(type="range")
          span
        span.helper Helper
    .s12.m6
      .field.border.label.invalid
        input
        label Label
        span.error Error
    .s12.m6
      .field.middle-align.invalid
        label.slider
          input(type="range")
          span
        span.error Error
    .s12.m6
      .field.border.label
        input
        label Label
        span.helper Helper
    .s12.m6
      .field.middle-align
        nav
          label.radio
            input(type="radio")
            span Item 1
          label.radio
            input(type="radio")
            span Item 2
          label.radio
            input(type="radio")
            span Item 3
        span.helper Helper
    .s12.m6
      .field.border.label.invalid
        input
        label Label
        span.error Error
    .s12.m6
      .field.middle-align.invalid
        nav
          label.radio
            input(type="radio")
            span Item 1
          label.radio
            input(type="radio")
            span Item 2
          label.radio
            input(type="radio")
            span Item 3
        span.error Error
    .s12.m6
      .field.border.label
        input
        label Label
        span.helper Helper
    .s12.m6
      .field.middle-align
        nav
          label.checkbox
            input(type="checkbox")
            span Item 1
          label.checkbox
            input(type="checkbox")
            span Item 2
          label.checkbox
            input(type="checkbox")
            span Item 3
        span.helper Helper
    .s12.m6
      .field.border.label.invalid
        input
        label Label
        span.error Error
    .s12.m6
      .field.middle-align.invalid
        nav
          label.checkbox
            input(type="checkbox")
            span Item 1
          label.checkbox
            input(type="checkbox")
            span Item 2
          label.checkbox
            input(type="checkbox")
            span Item 3
        span.error Error
    .s12.m6
      .field.border.label
        input
        label Label
        span.helper Helper
    .s12.m6
      .field.middle-align
        nav
          .max
            h6 Title
            div Some text here
          label.switch
            input(type="checkbox")
            span
        span.helper Helper
    .s12.m6
      .field.border.label.invalid
        input
        label Label
        span.error Error
    .s12.m6
      .field.middle-align.invalid
        nav
          .max
            h6 Title
            div Some text here
          label.switch
            input(type="checkbox")
            span
        span.error Error

</template>

<script setup lang="ts">
import { ref } from "vue";
import domain from "../home/domain";
import datePicker from "./datePicker/datePicker.vue";
const updateTheme = () => {
  document.body.className = document.body.className.indexOf("dark") !== -1 ? "light" : "dark";
};
const number = ref(0);
const text = ref();
const select = ref();
</script>
