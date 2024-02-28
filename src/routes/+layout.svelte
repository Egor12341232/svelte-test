<nav>
    <div class="nav-container">
    <a href="/" class="nav_logo" title="Black to Homepage">Prokofev Egor</a>
    <div class="nav-links">
        <!-- svelte-ignore missing-declaration -->
        {#each nav as link}

<a href={link.href} class="link">{link.title}{link.isShow}</a>

{/each}
    </div>
    </div>
    </nav>
    
    <div class="container">
    <!--Pages will be injected below-->
    <slot></slot>
    </div>
    <script>
        const nav =[
{
title: "Обо мне",
href: "/about",
isShow: true,
},

{
title: "Блог",
href: "/blog",
isShow: true,
},

{
title: "Портфолио",
href: "/project",
isShow: true,
},

{
title: "Контакты",
href: "/contact",
isShow: true,
},

{
title: "temp",
href: "/temp",
isShow: false,
},
];
    </script>
    <style>
    .container {
        max-width: 1400px;
        margin: 50px auto;
    }
    </style>