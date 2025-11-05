<template>
  <v-app>


     <v-navigation-drawer
       
      >
        <v-list>
          <v-list-item
            prepend-avatar="https://pbs.twimg.com/profile_images/1426180219061166081/ze9F3n7N_400x400.jpg"
            subtitle="DIT - 3B"
            title="Rafael Flores"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi mdi-account-file" title="My Files" value="myfiles"></v-list-item>
          <v-list-item prepend-icon="mdi mdi-folder-account" title="Shared with me" value="shared"></v-list-item>
          <v-list-item prepend-icon="mdi-star" title="Starred" value="starred"></v-list-item>
        </v-list>
      </v-navigation-drawer>

    <v-app-bar :elevation="6">
  <template v-slot:prepend>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
  </template>

  <v-app-bar-title>Application Bar</v-app-bar-title>
</v-app-bar>



    <v-main>
      <v-container>
        <slot />
      </v-container>
    </v-main>
  </v-app>
</template>
