<template lang="pug">
  h-page
    h-page-header(fixed)
      h-app-toolbar
        h-app-toolbar-container(bgcolor="bg-primary" textcolor="text-white")
          h-app-toolbar-navigation(icon="fas fa-bars" textcolor="text-white" @click="$refs.nav.open()")
          h-app-toolbar-title(title="HawkFramework")
          h-app-toolbar-action
            router-link(to="/yourpage")
              h-fa-icon(icon="fas fa-globe" textcolor="text-white")
            a(href='https://github.com/edutucci/hawkframework' target="_blank")
              h-fa-icon(icon="fab fa-github" textcolor="text-white")

    h-page-content(style="margin-top: 62px; margin-bottom: 62px;")
      router-view

    h-page-footer(fixed)
      .flex.flex-justify-center.flex-items-center.bg-primary.text-white(style="height: 60px")
        H3 HawkFramework Page Footer

</template>

<script>

export default {
  components: {
  },
  data () {
    return {
    }
  }
}
</script>
