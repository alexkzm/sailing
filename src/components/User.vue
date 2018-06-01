<template>
    <aside class="sidebar" data-js="sidebar">
    <ul class="sidebar__ul">
        <li>1</li>
        <li>2</li>
        <li>3></li>
    </ul>
    </aside>

    <g>
      <polygon :points="points"></polygon>
      <axis-lable v-for="(stat, index) in stats"></axis-lable>
    </g>

    <button class="button" data-js="open-sidebar" data-theme="button">Open Sidebar</button>


</template>

<script>
export default {
    
}
</script>

<style>
#sidebar {
    height: 100vh;
    position: fixed;
    top: 0;
    left: -200px;
    width: 100%;
    transition: left 0.3 s ease-in-out;
    transform: translate3d(-100%, 0, 0);
    background: rgba(111, 111, 111, 1);
}

.sidebar-open{
    transform: translate3d(0,0,0) !important;
}

themed {
    color: gold !important;
}

.body--themed [data-theme="button"] {
    color: gold;
}

@media screen and (min-width: 700px) {
    .sidebar__ul {
        flex: 0 0 200px;
    }
}

</style>

