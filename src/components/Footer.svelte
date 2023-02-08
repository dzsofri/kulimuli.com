<footer>
    <span class="brand">
        <img src="./logo.png" alt="">
        <span class="name">kulimuli.com</span>
    </span>
    <hr>
    <div class="links">
        <div class="documents">
            <!-- Links -->
            <a href="">Általános Szerződési Feltételek (ÁSZF)</a>
            <a href="">GYIK</a>
            <a href="">Adatvédelmi nyilatkozat</a>
            <a href="">Cookiek-ra vonatkozó szabályok</a>
        </div>
        <div class="socials">
            <!-- Socials -->
            <a href=""><img src="./facebook.png"></a>
            <a href=""><img src="./instagram.png"></a>
            <a href=""><img src="./youtube.png"></a>
            <a href=""><img src="./tiktok.png"></a>
            <a href=""><img src="./twitter.png"></a>
        </div>
    </div>
</footer>

<style lang="scss">
    footer {
        background-color: #D9D9D9;
        padding: 2.5rem;

        .brand {
            color: black;
            font-weight: bold;
            font-size: 2rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1rem;

            img {
                width: 5rem;
                border-radius: 100%;
            }
        }

        .links {
            margin-top: 1rem;
            display: flex;

            .documents {
                width: max-content;
                display: flex;
                flex-direction: column;
                gap: .5rem;

                & > * {
                    color: black;
                    text-decoration: none;
                }
            }

            .socials {
                width: 100%;
                display: flex;
                justify-content: space-evenly;
                align-items: center;
            }
        }
    }
</style>