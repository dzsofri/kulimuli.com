<div class="kuli_card_big">
    <div class="kuli_kep" style="background-image: url(./kulimakok/{kepId});"></div>
    <div class="leiras">
        <h1>{nev}</h1>
        <hr>
        <div class="tulajdonsagok">
            <span>
                <span class="bold">Kor:</span>
                <span>{kor}</span>
            </span>
            <span>
                <span class="bold">Nem:</span>
                <span>{nem}</span>
            </span>
            <!--<span>
                <span class="bold">Ritkaság:</span>
                <span>{ritkasag}</span>
            </span>-->
        </div>
        <button on:click={orokbefogadas}>Örökbefogadom</button>
    </div>
</div>

<style lang="scss">
    @media screen and (max-width: 600px) {
        .kuli_card_big {
            flex-direction: column;
            height: 500px !important;
        }

        .kuli_card_big .kuli_kep {
            border-radius: 25px 25px 0px 0px !important;
            flex-basis: 50% !important;
        }
        
        .kuli_card_big .leiras {
            flex-basis: 50% !important;
        }

        .kuli_card_big .leiras h1 {
            font-size: 1.5rem;
        }

        .kuli_card_big .tulajdonsagok {
            gap: .2rem !important;
        }

        .kuli_card_big button {
            font-size: 1.2rem !important;
            align-self: center !important;
        }
    }

    .kuli_card_big {
        display: flex;
        background-color: #F9F2ED;
        border-radius: 25px;
        position: relative;
        height: 350px;
    }

    .kuli_card_big .kuli_kep {
        flex-basis: 40%;
        background-image: url('./henrykettner.jpg');
        background-repeat: no-repeat;
        background-size: contain;
        background-position: center;
        // background-color: white;
        border-radius: 25px 0px 0px 25px;
        align-self: stretch;
    }

    .kuli_card_big .leiras {
        display: flex;
        flex-direction: column;
        flex-basis: 60%;
        box-sizing: border-box;
        padding: 1rem;
    }

    .kuli_card_big hr {
        margin: 1rem;
    }

    .kuli_card_big .tulajdonsagok {
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    .kuli_card_big .tulajdonsagok > span {
        display: flex;
    }

    .kuli_card_big .tulajdonsagok > span > span:nth-child(2) {
        align-self: flex-end;
        margin-left: auto;
    }

    button {
        background-color: #F87474;
        border-radius: 1000px;
        border: none;
        color: white;
        font-size: 1.3rem;
        padding: .5rem 1rem;
        cursor: pointer;

        margin-top: auto;
        align-self: flex-end;
    }

    button:hover {
        background-color: #d15c5c;
        border: #d15c5c;
    }

    .bold {
        font-size: larger;
        font-weight: bolder;
    }
</style>

<script lang="ts">
    export let kepId: number;
    export let nev: string;
    export let kor: number;
    export let nem: string;
    // export let ritkasag: string;

    function orokbefogadas() {
        alert("Örökbefogadva! A kiszállítást hamarosan megkezdjük.");
    }
</script>
