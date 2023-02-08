<main>
    <div class="gombdisplay">
        <span>Ennyiszer nyomtad meg A Gombot:</span>
        <span id="gombcucc">{gombnyomasok}</span>
    </div>

    <div class="video">
        <!-- svelte-ignore a11y-media-has-caption -->
        <video controls src="./video.mp4">
    </div>

    <button type="button" on:click={gombClick}>A gomb</button>
</main>

<style lang="scss">
    main {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        min-height: 93vh; // Ebbe ugye benne van a navbar merete kb
        align-items: center;
    }

    video {
        width: 100vw;
    }

    button{
        background-color: #FFB562;
        border: none;
        width: 30vw;
        height: 100px;
        font-size: 1.5rem;
        border-radius: 15px;
        transition: .2s;
        filter: drop-shadow(0 10px 8px rgb(0 0 0 / 0.04)) drop-shadow(0 4px 3px rgb(0 0 0 / 0.1))
    }

    button:hover {
        filter: brightness(.95);
        transform: scale(.95);
        transition: .2s;
        cursor: pointer;
        filter: drop-shadow(0 4px 3px rgb(0 0 0 / 0.07)) drop-shadow(0 2px 2px rgb(0 0 0 / 0.06));;
    }

    .gombdisplay {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    #gombcucc {
        font-weight: 600;
        font-size: 36px;
    }
</style>

<script lang="ts">
    let gombnyomasok = 0;

    function gombClick() {
        gombnyomasok += 1;
    }
</script>
