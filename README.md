<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script>
        function triggerAnimation() {
            const imagea = document.getElementById("Egg.png");
            
            // Add the animation class
            imagea.classList.add("animate");

            setTimeout(rickRoll,2000);

        }
        function rickRoll() {
            const Url = "https://www.youtube.com/watch?v=QDia3e12czc";
            window.location.href = Url;
        }
    </script>
    <style>
        html, body {
            width: 100vw;
            height: 100vh;
            /* Inset shadow with a large blur radius */
            box-shadow: 0 0 200px rgba(42, 42, 42, 0.9) inset;
            background-color: rgb(91, 91, 91); /* Background color for the page/element */
            margin: 0; /* Removes default browser margin */
            padding: 0; /* Removes default browser padding */
            overflow: hidden; /* Hides both horizontal and vertical scrollbars */
        }
        /* Optional: Style for a container div to hold your content */
        .flex-container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100%;
            width: 100%;
        }
        .Egg {
            animation-name: spin;
            animation-duration: 2s;
            animation-timing-function: cubic-bezier(.68,.95,.72,1);
            animation-fill-mode: forwards;
            filter: drop-shadow(0 0 50px #ffe68dd1);
        }
        @keyframes spin {
            from{
                transform: translateY(-1000px) rotate(-20deg);
            }
            to{
                transform: translateY(0px) rotate(20deg);
                
            }
        }
        @keyframes bounce {
            from{

            }
            to{
                transform: translateY(1000px)
                
            }
        }
        .animate {
            animation-name: bounce;
            animation-duration: 1.5s;
            animation-timing-function: ease-in;
            animation-fill-mode: forwards;
        }  

    </style>
</head>
<body>
    <div class="flex-container" id="myContainer">
        <img style="height: 45%; " src="Egg.png" onclick="triggerAnimation()" class="Egg">
    </div>    
</body>
</html>
