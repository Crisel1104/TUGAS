<template>
    <div class="main-sidebar">
        <aside id="sidebar-wrapper">
          <div class="sidebar-brand">
            <a href="index.html">Fullstack Academy</a>
          </div>
          <div class="sidebar-brand sidebar-brand-sm">
            <a href="index.html">FA</a>
          </div>
          <ul class="sidebar-menu">
              <!-- <li class="menu-header">Dashboard</li>
              <li class="nav-item dropdown">
                <a href="#" class="nav-link has-dropdown"><i class="fas fa-fire"></i><span>Dashboard</span></a>
                <ul class="dropdown-menu">
                  <li><a class="nav-link" href="index-0.html">General Dashboard</a></li>
                  <li><a class="nav-link" href="index.html">Ecommerce Dashboard</a></li>
                </ul>
              </li> -->
            <li v-for="(menu,i) in listMenu" :key="i">
              <nuxt-link class="nav-link" :to="menu.to">
                <i :class="menu.icon"></i> <span>{{menu.name}}</span>
              </nuxt-link>
            </li>  
          </ul>
        </aside>
      </div>
</template>

<script>
export default {
  data() {
    return {
      listMenu: [
        {
          name: "Dashboard",
          to: "/",
        },
        {
          name: "List Class",
          to: "/kelas",
        },
        {
          name: "Presensi",
          to: "/",
        },
      ]
    }
  }
}
</script>