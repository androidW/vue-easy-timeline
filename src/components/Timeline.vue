<template>
  <ul class="timeline" type="both">
    <li class="timeline-title">
      <div class="icon" />
      <div class="title">2021.06.13</div>
      <div class="comment">备注</div>
    </li>
    <li class="timeline-item">
      <div class="icon" />
      <div class="title">2021.06.13</div>
      <div class="comment">备注</div>
    </li>
    <li>test1</li>
    <li>test1</li>
  </ul>
</template>

<script>
export default {
  name: 'Timeline',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.timeline {
  position: relative;
  list-style-type: none;
  padding: 0;
  word-break: break-word;
}

.timeline li:not(:first-child) {
  margin-top: 2rem;
}

.timeline .timeline-title + .timeline-item {
  margin-top: 0.5rem;
}

.timeline[type="single"] {
  left: 1rem;
}

.timeline[type="both"] {
  left: 50%;
  width: 50%;
}

.timeline[type="both"] .timeline-title {
  width: 200%;
  margin-left: -100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.timeline[type="both"] .timeline-title>.icon {
  margin-left: 0;
}

.timeline[type="both"] .timeline-title>.title {
  width: 50%;
  transform: translateY(-50%);
  text-align: right;
  align-self: center;
  order: 0;
  flex: 1;
  margin-right: 1rem;
}

.timeline[type="both"] .timeline-title>.comment {
  width: 50%;
  align-self: center;
  order: 2;
  text-align: left;
  flex: 1;
  transform: translateY(-50%);
  margin-left: 1rem;
}

.timeline::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 0.1rem;
  height: 100%;
  background: #000;
  z-index: 0;
}

.timeline-title .icon {
  position: absolute;
  width: 0.5rem;
  height: 0.5rem;
  border-radius: 100%;
  background: rgb(180, 180, 180);
  margin-left: -0.2rem;
  z-index: 1;
}
</style>
