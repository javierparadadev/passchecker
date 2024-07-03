<template>
  <div class="item">
    <i>
      <slot name="icon"></slot>
    </i>
    <div class="details">
      <h3>
        <slot name="heading"></slot>
      </h3>

      <slot></slot>

      <progress class="progress is-success is-small" value="60" max="100"/>
    </div>
    
  </div>
</template>

<style src="./styles.css" scoped></style>
