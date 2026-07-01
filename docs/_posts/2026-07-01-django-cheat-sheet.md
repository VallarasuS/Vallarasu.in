---
layout: post
category: Python
---

<style>
    body {
        filter: none !important;
        background: #000000;
        color: white;
    }

    a {
        color: #ffff10;
    }

    code {
        background: #2d2d2d;
        border-radius: 5px;
    }

    pre { 
        line-height: 125%; 
    }

    .highlight {
        background: #000000;
        color: #cccccc;
    }

    .highlight .hll { background-color: #222222; }

    /* Comments */
    .highlight .c, .highlight .ch, .highlight .cm, 
    .highlight .cp, .highlight .cpf, .highlight .c1 { 
        color: #00d600; 
    }

    /* Keywords */
    .highlight .k, .highlight .kc, .highlight .kd, 
    .highlight .kn, .highlight .kp, .highlight .kr, 
    .highlight .kt, .highlight .ow { 
        color: #cdcd00; 
    }

    /* Strings */
    .highlight .s, .highlight .sa, .highlight .sb, .highlight .sc, 
    .highlight .dl, .highlight .sd, .highlight .s2, .highlight .se, 
    .highlight .sh, .highlight .si, .highlight .sx, .highlight .sr, 
    .highlight .s1, .highlight .ss { 
        color: #ed9d13; 
    }

    /* Numbers */
    .highlight .m, .highlight .mb, .highlight .mf, .highlight .mh, 
    .highlight .mi, .highlight .mo, .highlight .il { 
        color: #cd00cd; 
    }

    /* Builtins & Names */
    .highlight .nb, .highlight .bp { 
        color: #cd00cd; 
    }

    .highlight .nc, .highlight .nv, .highlight .vc, .highlight .vg, 
    .highlight .vi, .highlight .vm { 
        color: #00cdcd; 
    }

    /* Operators */
    .highlight .o { 
        color: #3399cc; 
    }

    /* Special */
    .highlight .cs { 
        color: #cd0000; 
        font-weight: bold; 
    }

    .highlight .err { 
        color: #cccccc; 
        border: 1px solid #FF0000; 
    }

    .code {
        font-size: 14px;
    }
</style>

#### Contents

1. [Installation and Setup](#installation-and-setup)
1. [Django CLI](#variables-and-data-types)


## Installation and Setup
```shell
c:\> py -m pip install django
```

## Django CLI

```shell
c:\> django-admin startproject project-name .
c:\> py manage.py startapp app-name
c:\> py manage.py runserver
```

<style>
    .highlight:hover {
        svg {
            visibility: visible
        }
    }

    svg {
        visibility: hidden
    }
</style>

<template id="copy-icon-template">
    <div id="copy-icon" style="width: 16px; height: 16px; border-radius: 5px; position: absolute; right: 10px; top: 10px; padding: 10px;
        border-radius: 5px;" onmouseenter="this.style.background='#715A5A'"
        onmouseleave="this.style.background='transparent'" onmousedown="this.style.background='black'"
        onmouseup="this.style.background='transparent'" onclick="copy(this)">

        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" fill="white">
            <path
                d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z">
            </path>
            <path
                d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z">
            </path>
        </svg>

    </div>
</template>

<script>

    copy_template = document.getElementById("copy-icon-template")
    codes = document.getElementsByTagName("code")

    for (let code of codes) {
        parent = code.parentNode.parentNode
        parent.style.position = "relative"
        el_copy = copy_template.content.cloneNode(true)
        parent.appendChild(el_copy)
    }

    function copy(e) {
        navigator.clipboard.writeText(e.parentNode.firstElementChild.textContent)
    }

</script>

