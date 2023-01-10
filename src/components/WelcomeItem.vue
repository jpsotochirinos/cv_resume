<script setup>
  import { ref } from "vue";
  import { KinesisContainer, KinesisElement, KinesisDistance} from "vue-kinesis"
  let details = ref(false)
  const emit = defineEmits(['customChange_child_child'])
  const showDetails = ()=>{
    //details.value = !details.value
    emit('customChange_child_child')
  }
</script>
<template>
  <div class="item">
    

    <i>
    <v-btn
    class="mx-2"
    outlined
    color="purple"
    @click="showDetails"
    >
    <kinesis-container>
      <kinesis-element :strength="10" axis="y">
      <slot name="icon"></slot>
      </kinesis-element>
    </kinesis-container>
    </v-btn>
      
    </i>
  
    
    <div  class="details">
      <h3>
        <kinesis-container>
          <kinesis-element :strength="10" axis="x">
          <slot name="heading"></slot>
          </kinesis-element>
        </kinesis-container>
      </h3>
      <slot v-if="details" name="details"></slot>
    </div>
  </div>
</template>

<style scoped>
.item {
  margin-top: 2rem;
  display: flex;
}

.details {
  flex: 1;
  margin-left: 3rem;
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  width: 32px;
  height: 32px;

  color: var(--color-text);
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0rem;
  color: var(--color-heading);
}

@media (min-width: 200px) {
  .item {
    margin-top: 0;
    padding: 2.4rem 0 2.4rem calc(var(--section-gap) / 2);
  }

  i {
    top: calc(50% - 25px);
    left: 2.5rem;
    position: absolute;
    
    background: var(--color-background);
    border-radius: 8px;
    width: 50px;
    height: 50px;
  }

  .item:before {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 4rem;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:after {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 4rem;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }
}
</style>
