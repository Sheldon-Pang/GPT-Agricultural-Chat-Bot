<script lang="ts">
	import type { ChatCompletionRequestMessageRoleEnum } from 'openai'
	export let type: ChatCompletionRequestMessageRoleEnum
	export let message: string
</script>

<div class="chat {type === 'user' ? 'chat-end' : 'chat-start'} justify-end">
	<div class="chat-image avatar">
		<div class="w-10 rounded-full">
			<img
				src="https://ui-avatars.com/api/?name={type === 'user' ? '我' : 'AI'}"
				alt="{type} avatar"
			/>
		</div>
	</div>
	<div class="chat-header">
		{type === 'user' ? '我' : 'AI人工智能'}
	</div>
	<div class="chat-bubble {type === 'user' ? 'chat-bubble-primary' : 'chat-bubble-secondary'}">
		{message}
	</div>
</div>

<style>
	.chat-bubble-primary {
	  /* Color for the user's chat bubble */
	  background-color: #3695e3;
	  color: #ffffff;
	}
	.chat-bubble-secondary {
	  /* Color for the AI's chat bubble */
	  background-color: #3695e3;
	  color: #ffffff;
	}
</style>
	