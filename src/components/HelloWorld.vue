<template>
  <div>
    <div class="nth-child-class">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
      <div>5</div>
      <div>6</div>
      <div>
        <div>7</div>
        <div>8</div>
        <div>9</div>
        <div>0</div>
        <div>11</div>
      </div>
    </div>
    <div class="nth-child-class">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
      <div>5</div>
      <div>6</div>
      <div>7</div>
    </div>
    <div class="nth-child-class">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
      <div>5</div>
      <div>6</div>
      <div>7</div>
    </div>
    <div class="nth-child-class">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
      <div>5</div>
      <div>6</div>
      <div>7</div>
    </div>
    <div class="nth-child-class">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
      <div>5</div>
      <div>6</div>
      <div>7</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {
    
  }
}
</script>

<style scoped>
div {
  margin-bottom: 20px; 
}
div:last-child {
  margin-bottom: 0;
}
</style>
