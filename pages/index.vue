<template>
	<v-layout justify-center align-center wrap>
		<v-flex xs12 sm8 md6>
			<template v-for="(idea,index) in ideas">
				<v-card :key="index" class="my-2 align-content-space-between flex-wrap">
					<v-card-title>
						<p class="headline">{{idea.title}}</p>
					</v-card-title>
					<v-card-text>

					</v-card-text>
					<v-card-actions>
						<p>{{idea.like}}いいね<v-icon class="align-start">mdi_favorite_border</v-icon></p>
					</v-card-actions>
				</v-card>
			</template>
		</v-flex>
	</v-layout>
</template>

<script>

export default {
	data: ()=>({
		ideas: [
			{
				title:"〜〜〜が欲しい！",
				like: 0,
				cont:"木下",		//ユーザーIDになるかも
				commentsNum: 0
			},
			{
				title:"〜〜〜なアイデア",
				like: 10,
				cont:"守時",		//ユーザーIDになるかも
				commentsNum: 21
			}
		]
	})
}
</script>
