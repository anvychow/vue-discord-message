<template>
	<div :class="{ 'discord-inline-field': inline }" class="discord-embed-field">
		<div class="discord-field-title">{{ title }}</div>
		<slot></slot>
	</div>
</template>

<script>
export default {
	name: 'EmbedField',
	props: {
		title: {
			type: String,
			required: true,
		},
		inline: Boolean,
	},
};
</script>

<style>
.discord-embed .discord-embed-field {
	min-width: 100%;
	margin-top: 5px;
}

.discord-embed .discord-embed-field.discord-inline-field {
	flex-grow: 1;
	flex-basis: auto;
	min-width: 150px;
}

.discord-embed .discord-embed-field .discord-field-title {
	color: #72767d;
	font-weight: 500;
	margin-bottom: 2px;
}

.discord-light-theme .discord-embed .discord-embed-field .discord-field-title {
	color: #747f8d;
}
</style>
