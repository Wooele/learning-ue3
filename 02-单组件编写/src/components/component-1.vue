<template>
  <p class="msg" ref="msg">{{ msg }}</p>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

interface Member {
	id: number,
	name: string
};
export default defineComponent({
  setup () {
    
    const msg = 'Hello World!';
		// 使用自定义对象格式
    const userInfo = ref<Member>({
        id: 1,
        name: 'Tom'
    });
		// 数字数组
		const uids = ref<number[]>([1, 2, 3]);
		// 字符串数组
		const names = ref<string[]>(['Tom', 'Petter', 'Andy']);
		// 定义一个成员组
		const memberList = ref<Member[]>([
			{
				id: 1,
				name: 'Tom'
			},
			{
				id: 2,
				name: 'Petter'
			},
			{
				id: 3,
				name: 'Andy'
			}
		])

    return {
      msg
    }
  }
})
</script>

<style lang="stylus" scoped>
.msg
  font-size 14px
</style>

<style scoped>
.msg{
    font-size: 14px;
}
</style>