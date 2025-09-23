---
layout: post
category: 30Days
author: sivakami
---

console.log(site.data.videos);

{% assign days = site.data.videos[post.author].days | default: 0 %}
{% assign entries = site.data.videos[post.author].posts | default: [] %}

<div> 

    <style type="text/css">

        .grayscale {
            filter: grayscale();
        }

        .heart {
            height: 15px !important;
        }

        ul {
            list-style: none;
        }

        li {
            margin-top: 10px;
        }
    </style>

    <template id="tracker-hearts">
        <div style="
            margin: 20px 0px; 
            border: 1px solid #8c8c8cc4; 
            border-radius: 5px; 
            padding: 20px 20px; 
            width: auto;
            border-style: dashed;">

            <div style="display: flex; flex-direction: row">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
            </div>

            <div style="display: flex; flex-direction: row">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
            </div>

            <div style="display: flex; flex-direction: row">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
                <img class="heart grayscale" src="../assets/images/heart.png">
            </div>

            <div style="display: flex; justify-content: space-between; margin-top: 10px;">
                <span id="user-name" style="font-size: smaller; color: #f9595f;"> Vallarasu </span>
                <span id="user-days" style="font-size: smaller; color: #f9595f;"> Vallarasu </span>
            </div>

        </div>
    </template>

    <div class="container" style="
            border: 1px solid #8c8c8cc4; 
            border-radius: 5px; 
            padding: 20px 20px; 
            width: auto;
            border-style: solid;">

        <div style="display: flex; flex-direction: column;">

            <img style="width: 150px; border-radius: 75px;" src="../assets/images/rajamatha.png">

            <span style="font-size: larger; margin-top: 10px;"> {{ author.name }} </span>

            <span style="font-size: smaller; margin: 10px 0px;"> {{ author.description }} </span>

            <div style="display: flex; flex-direction: row; gap: 10px; font-size: smaller;">
                <a target="_blank" href="{{ author.li }}">LinkedIn</a>
                <a target="_blank" href="{{ author.insta }}">Instagram</a>
                <a target="_blank" href="{{ author.x }}">X</a>
            </div>

            <hr style="width: 100%; margin: 20px 0px; border-style: dashed;">

            <span style="font-size: smaller; margin-top: 10px;">30 Days 30 Videos Challenge</span>

            <div id="tracker-container"></div>

            <ul>
            {% for entry in entries %}
                <li>
                    <a target="_blank" href="{{ entry.url }}"> {{ entry.title }} </a>
                </li>
            {% endfor %}
            </ul>

        </div>

    </div>

    <script>

        let users = [
            { todo: {{ days }}, name: "{{ page.author }}" },
        ]

        const container = document.querySelector("#tracker-container")

        users.forEach(u => {

            const trackerTemplate = document.querySelector("#tracker-hearts");
            const instance = trackerTemplate.content.cloneNode(true);
            const name = instance.querySelector("#user-name");
            name.textContent = u.name;

            instance.querySelectorAll("img").forEach((ig, i) => {
                if (i < u.todo) {
                    ig.classList.remove("grayscale");
                }
            });

            const days = instance.querySelector("#user-days");
            days.textContent = `${u.todo} days`;

            container.appendChild(instance);
        });
    </script>

</div>