<template>
	<v-app>
		<v-app-bar app></v-app-bar>
		<v-navigation-drawer model="drawer" app>
			<v-list>
				<v-list-item v-for="room in rooms" :key="room.id" link>
					<v-list-item-content>
						<v-list-item-title>{{ room.title }}</v-list-item-title>
						<v-list-item-subtitle>{{ room.lastMessage }}</v-list-item-subtitle>
					</v-list-item-content>
				</v-list-item>
			</v-list>
		</v-navigation-drawer>
		<v-main>
			<v-container fluid="true">
				<v-row>
					<v-btn class="d-flex flex-center align-center">Connect wallet</v-btn>
				</v-row>
			</v-container>
		</v-main>
		<v-footer app></v-footer>
	</v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    drawer: null,
	rooms: [
		{ id: 1, title: '0x00', lastMessage: 'Hello 1' },
		{ id: 2, title: '0x01', lastMessage: 'Hello 2' }
	]
  }),
};
</script>
