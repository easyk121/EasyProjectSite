# EasyProjectSite
Site with MIT License, File and Github. Coded by ChatGPT.

https://testing-weasy.netlify.app/ for example

COPY THIS CODE:
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Easy's Project</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Segoe UI',sans-serif;
}

body{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(-45deg,#0f172a,#1e293b,#312e81,#0f172a);
    background-size:400% 400%;
    animation:gradient 15s ease infinite;
    overflow:hidden;
}

/* Background particles */
.circle{
    position:absolute;
    border-radius:50%;
    background:rgba(255,255,255,.04);
    animation:float linear infinite;
}

.c1{
    width:150px;
    height:150px;
    top:10%;
    left:10%;
    animation-duration:18s;
}

.c2{
    width:220px;
    height:220px;
    bottom:10%;
    right:10%;
    animation-duration:24s;
}

.c3{
    width:90px;
    height:90px;
    top:15%;
    right:20%;
    animation-duration:14s;
}

.container{
    text-align:center;
    z-index:1;
}

h1{
    color:white;
    font-size:4rem;
    margin-bottom:30px;
    text-shadow:0 0 25px rgba(255,255,255,.15);
}

.buttons{
    display:flex;
    gap:15px;
    justify-content:center;
    flex-wrap:wrap;
}

.btn{
    border:none;
    cursor:pointer;
    padding:16px 30px;
    border-radius:16px;

    color:white;
    font-size:16px;
    text-decoration:none;

    background:rgba(255,255,255,.08);
    backdrop-filter:blur(10px);

    transition:.25s;
}

.btn:hover{
    transform:translateY(-4px);
    background:rgba(255,255,255,.15);
}

/* MODAL */

.modal{
    display:none;
    position:fixed;
    inset:0;
    z-index:999;

    background:rgba(0,0,0,.65);
    backdrop-filter:blur(8px);
}

.modal.show{
    display:block;
}

.modal-content{
    width:min(900px,90%);
    max-height:80vh;
    overflow:auto;

    margin:60px auto;
    padding:25px;

    border-radius:20px;

    background:rgba(20,20,30,.95);

    color:white;

    animation:popup .25s ease;
}

.close{
    float:right;
    font-size:32px;
    cursor:pointer;
    user-select:none;
}

.modal h2{
    margin-bottom:20px;
}

/* FILE LIST */

.file-row{
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:20px;

    padding:18px;
    margin-bottom:15px;

    border-radius:14px;

    background:rgba(255,255,255,.05);
}

.file-info{
    flex:1;
}

.file-name{
    font-size:18px;
    font-weight:600;
}

.file-desc{
    margin-top:5px;
    opacity:.8;
}

.download{
    text-decoration:none;
    color:white;

    padding:12px 18px;

    border-radius:12px;

    background:rgba(255,255,255,.1);

    transition:.2s;
}

.download:hover{
    background:rgba(255,255,255,.18);
}

/* RULES */

.rule-box{
    padding:20px;
    border-radius:14px;
    background:rgba(255,255,255,.05);
}

.rule-box ul{
    margin-left:20px;
    margin-top:10px;
}

.rule-box li{
    margin-bottom:10px;
}

/* ANIMATIONS */

@keyframes popup{
    from{
        opacity:0;
        transform:scale(.95);
    }
    to{
        opacity:1;
        transform:scale(1);
    }
}

@keyframes gradient{
    0%{background-position:0% 50%;}
    50%{background-position:100% 50%;}
    100%{background-position:0% 50%;}
}

@keyframes float{
    from{
        transform:translateY(0) rotate(0deg);
    }
    to{
        transform:translateY(-60px) rotate(360deg);
    }
}

@media(max-width:700px){

    h1{
        font-size:2.7rem;
    }

    .file-row{
        flex-direction:column;
        align-items:flex-start;
    }

    .download{
        width:100%;
        text-align:center;
    }
}
</style>
</head>
<body>

<div class="circle c1"></div>
<div class="circle c2"></div>
<div class="circle c3"></div>

<div class="container">

    <h1>Easy's Project</h1>

    <div class="buttons">

        <a class="btn"
           href="https://github.com/easyk121/"
           target="_blank">
            GitHub
        </a>

        <button class="btn"
                onclick="openModal('filesModal')">
            Files
        </button>

        <button class="btn"
                onclick="openModal('rulesModal')">
            Rules & License
        </button>

    </div>

</div>

<!-- FILES MODAL -->

<div class="modal" id="filesModal">

    <div class="modal-content">

        <span class="close"
              onclick="closeModal('filesModal')">
              ×
        </span>

        <h2>📁 Files</h2>

        <div class="file-row">
            <div class="file-info">
                <div class="file-name">
                    Project-v1.0.zip
                </div>

                <div class="file-desc">
                    Latest stable release.
                </div>
            </div>

            <a class="download"
               href="files/Project-v1.0.zip"
               download>
               Download
            </a>
        </div>

        <div class="file-row">
            <div class="file-info">
                <div class="file-name">
                    Source-Code.zip
                </div>

                <div class="file-desc">
                    Complete source code package.
                </div>
            </div>

            <a class="download"
               href="files/Source-Code.zip"
               download>
               Download
            </a>
        </div>

        <div class="file-row">
            <div class="file-info">
                <div class="file-name">
                    Assets-Pack.zip
                </div>

                <div class="file-desc">
                    Images, icons and resources.
                </div>
            </div>

            <a class="download"
               href="files/Assets-Pack.zip"
               download>
               Download
            </a>
        </div>

    </div>

</div>

<!-- RULES MODAL -->

<div class="modal" id="rulesModal">

    <div class="modal-content">

        <span class="close"
              onclick="closeModal('rulesModal')">
              ×
        </span>

        <h2>📜 Rules & License</h2>

        <div class="rule-box">

            <h3>Rules</h3>

            <ul>
                <li>Do not claim ownership.</li>
                <li>Do not remove credits.</li>
                <li>Follow the license terms.</li>
                <li>Respect project usage conditions.</li>
            </ul>

            <br>

            <h3>License</h3>

            <p>
                MIT License
                <br><br>
                Copyright © Easy
                <br><br>
                Permission is hereby granted,
                free of charge, to any person
                obtaining a copy of this software.
            </p>

        </div>

    </div>

</div>

<script>
function openModal(id){
    document.getElementById(id).classList.add("show");
}

function closeModal(id){
    document.getElementById(id).classList.remove("show");
}

window.onclick = function(event){

    document.querySelectorAll(".modal").forEach(modal => {

        if(event.target === modal){
            modal.classList.remove("show");
        }

    });

};
</script>
</body>
</html>
```
**thanks guy for checking**
