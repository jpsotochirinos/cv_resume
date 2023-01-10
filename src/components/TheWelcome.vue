<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
const emit = defineEmits(['customChange_child'])
const handleCustomChange = (a)=>{

  emit('customChange_child',a)
}
</script>

<template>
  <div>
    <WelcomeItem @customChange_child_child="handleCustomChange(1)">
      <template #icon><DocumentationIcon /></template>
      <template #heading>About me</template>
    
    </WelcomeItem>

    <WelcomeItem @customChange_child_child="handleCustomChange(2)">
      <template #icon><ToolingIcon/></template>
      <template #heading>Experience</template>
      
    </WelcomeItem>

    <WelcomeItem @customChange_child_child="handleCustomChange(3)">
      <template #icon><EcosystemIcon/></template>
      <template #heading>Projects</template>
    </WelcomeItem>

    <WelcomeItem @customChange_child_child="handleCustomChange(4)">
      <template #icon><CommunityIcon/></template>
      <template #heading>Publications</template>
      
    </WelcomeItem>

    <WelcomeItem @customChange_child_child="handleCustomChange(5)">
      <template #icon><SupportIcon/></template>
      <template #heading>Designs</template>
    </WelcomeItem>
  </div>
</template>
