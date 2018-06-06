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

    <div class="content">
            {{{ post.content.rendered }}}
    </div>


</template>

<script>

    function delayed(delayMilliseconds, iterable) {
        return {
            [Symbol.asyncIterator]: function() {
                const iterator = iterable[Symbol.asyncIterator]()
                const delayedIterable = {
                    next: () => {
                        return delay(delayMilliseconds).then(() => iterator.next())
                    }
                }
                return delayedIterable
            }
        }
    }

    document.body.classList.toggle("body--themed")

export default {
    
}

    //Error handling
    if(!ul) throw new Error("Could not find [data-js-list]")
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

:focus {
    outline: 2px solid orange;
}

.body--themed [data-theme="button"] {
    color: gold;
}

button:hover {
    cursor: pointer;
}

@media screen and (min-width: 700px) {
    .sidebar__ul {
        flex: 0 0 200px;
    }
}

</style>

