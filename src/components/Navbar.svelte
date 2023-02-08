<nav>
    <div class="mobile" {hidden}>
        <a href="/">Főoldal</a>
        <a href="/kulimakok">Kulimákok</a>
        <a href="/gomb">Gomb</a>
        <a href="/rolunk">Rólunk</a>
        <a href="" on:click={kosar}>Kosár</a>
    </div>
    <div class="desktop">
        <a href="/"><img src="./logo.png" alt=""></a>
        <div class="linkek">
            <a href="/">Főoldal</a>
            <a href="/kulimakok">Kulimákok</a>
            <a href="/gomb">Gomb</a>
            <a href="/rolunk">Rólunk</a>
        </div>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <span class="material-symbols-outlined" id="menu_icon" on:click={toggleMobileNav}>
            menu
        </span>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <span class="material-symbols-outlined" id="kosar_icon" on:click={kosar}>
            shopping_cart
        </span>
    </div>
</nav>

<style lang="scss">
    #menu_icon, #kosar_icon {
        cursor: pointer;
    }
    
    @media screen and (max-width: 740px) {
        .desktop {
            justify-content: space-between !important;

            .linkek {
                display: none !important;
            }

            #kosar_icon {
                display: none;
            }
        }
    }

    @media screen and (min-width: 741px) {
        .mobile {
            display: none !important;
        }

        #menu_icon {
            display: none;
        }
    }

    .desktop {
        position: relative; // ha ez nincs itt akkor nem mukodik a z-index bruh
        z-index: 10;
        padding: 0 1rem 0 1rem;
        display: flex;
        justify-content: center;
        box-sizing: border-box;
        align-items: center;
        background-color: #FCFCFC;
        box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
        gap: 3rem;

        * {
            z-index: inherit;
        }

                
        & > *:first-child {
            justify-self: flex-start;
            margin-right: auto;

            img {
                height: 3rem;
                border-radius: 100%;
            }
        }


        & > *:last-child {
            margin-left: auto;
            font-size: 42px;
        }

        .linkek {
            display: flex;
            gap: 2rem;
        }

        .linkek > * {
            background-color: #FFB562;
            padding: .3rem 1rem .3rem 1rem;
            border-radius: 100px;
            color: #FCFCFC;
            text-decoration: none;
            transition: padding .3s;

            &:hover {
                padding: .3rem 1.5rem .3rem 1.5rem;
                transition: padding .3s;
            }
        }
    }

    .mobile {
        width: inherit;
        z-index: 5;
        position: absolute;
        display: flex;
        flex-direction: column;
        align-items: center;
        top: 0;
        margin-top: 3rem;
        background-color: #FCFCFCee;
        padding: 1.5rem;
        gap: 1rem;
        transition: transform .3s;
        box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);

        * {
            color: black;
        }
    }

    .mobile[hidden] {
        // max-height: 4rem !important;
        transform: translateY(-100%);
        transition: transform .3s;
    }

    nav {
        width: 100vw;
        height: 4rem;
    }
</style>

<script lang="ts">
    let hidden = true;

    function toggleMobileNav() {
        hidden = !hidden;
    }

    function kosar() {
        alert("A kosár jelenleg nem elérhető!");
    }
</script>