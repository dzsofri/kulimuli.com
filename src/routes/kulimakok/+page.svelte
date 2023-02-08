<main>
    <div class="kuli_filter">
        <h1>Kulifilter</h1>
        <div class="fajta_wrapper">
            <span>Fajta:</span>
            <input bind:value={filterNev} type="text" name="Fajta" id="ul_fajta">
        </div>
        <div class="nem_wrapper">
            <span>Nem:</span>
            <input type="radio" name="nem" id="him" value={"him"} bind:group={filterNem}>
            <label for="him">Hím</label>
    
            <input type="radio" name="nem" id="nosteny" value={"nosteny"} bind:group={filterNem}>
            <label for="nosteny">Nőstény</label>
        </div>
        <div class="kor_wrapper">
            <span>Kor:</span>
            <RangeSlider values={[0, 150]} min={0} max={150} pushy range on:change={(e) => {
                adjustFilterVals(e);
            }}></RangeSlider>
            <span>{filterKorMin} - {filterKorMax}</span>
        </div>
    </div>
    <div class="kulimakok">
        {#each kulakok as kuli}
            <KulimakKartya
                kepId={kulik.findIndex(x => x.nev == kuli.nev) + 1}
                nev={kuli.nev}
                kor={kuli.kor}
                nem={kuli.nem == "him" ? "hím" : "nőstény"} />
        {/each}
    </div>
</main>

<style lang="scss">
    @media screen and (max-width: 600px) {
        main {
            padding: 1rem !important;
        }

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

    main {
        padding: 3rem 5rem;
    }

    .kuli_filter h1 {
        margin-bottom: 1rem;
    }

    .kuli_filter {
        display: flex;
        flex-direction: column;
        gap: .5rem;
    }

    .kulimakok {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        margin-top: 1rem;
        background-color: #FFB562;
        border-radius: 10px;
        padding: 1rem;
    }

    .kulimakok .kuli_card_big {
        display: flex;
        background-color: #F9F2ED;
        border-radius: 25px;
        position: relative;
        height: 350px;
    }

    .kulimakok .kuli_card_big .kuli_kep {
        flex-basis: 40%;
        background-image: url('./henrykettner.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        border-radius: 25px 0px 0px 25px;
        align-self: stretch;
    }

    .kulimakok .kuli_card_big .leiras {
        display: flex;
        flex-direction: column;
        flex-basis: 60%;
        box-sizing: border-box;
        padding: 1rem;
    }

    .kulimakok .kuli_card_big hr {
        margin: 1rem;
    }

    .kulimakok .kuli_card_big .tulajdonsagok {
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    .kulimakok .kuli_card_big .tulajdonsagok > span {
        display: flex;
    }

    .kulimakok .kuli_card_big .tulajdonsagok > span > span:nth-child(2) {
        align-self: flex-end;
        margin-left: auto;
    }

    .kulimakok button {
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

    .kulimakok button:hover {
        background-color: #d15c5c;
        border: #d15c5c;
    }

    .bold {
        font-size: larger;
        font-weight: bolder;
    }

    #ul_fajta {
        width: 50%;
        padding: .2rem;
        background-color: #D9D9D9;
        border: none;
    }
</style>

<script lang="ts">
	import RangeSlider from 'svelte-range-slider-pips';
    import KulimakKartya from "../../components/KulimakKartya.svelte";
    import destr from 'destr';
	import Footer from '../../components/Footer.svelte';

        // eskuszom irtam erre egy apit de a svelte akkora egy szar hogy
    // nem kepes betolteni
    const kulik: KuliDTO[] = [
        {
            nev: '6ix9ine Kulimák',
            kor: 42,
            nem: 'nosteny',
        },
        {
            nev: 'Angry Birds Kulimák',
            kor: 7,
            nem: 'him',
        },
        {
            nev: 'Bank rabló Kulimák',
            kor: 36,
            nem: 'him',
        },
        {
            nev: 'Bilihajú Kulimák',
            kor: 16,
            nem: 'him',
        },
        {
            nev: 'Biznisz Kulimák',
            kor: 24,
            nem: 'him',
        },
        {
            nev: 'cowboy Kulimák',
            kor: 16,
            nem: 'him',
        },
        {
            nev: 'Erõs Kulimák',
            kor: 24,
            nem: 'him',
        },
        {
            nev: 'Evõs Kulimák',
            kor: 100,
            nem: 'him',
        },
        {
            nev: 'Fiatal Kulimák',
            kor: 5,
            nem: 'him',
        },
        {
            nev: 'Fizika tanár Kulimák',
            kor: 99,
            nem: 'him',
        },
        {
            nev: 'Flexbox Froggyzó Kulimák',
            kor: 17,
            nem: 'him',
        },
        {
            nev: 'Fortnite player Kulimák',
            kor: 9,
            nem: 'him',
        },
        {
            nev: 'Jimmy Neutron Kulimák',
            kor: 21,
            nem: 'him',
        },
        {
            nev: 'Kakilós Kulimák',
            kor: 17,
            nem: 'him',
        },
        {
            nev: 'Kanye és Kulimák',
            kor: 42,
            nem: 'him',
        },
        {
            nev: 'Kopasz Kulimák',
            kor: 17,
            nem: 'him',
        },
        {
            nev: 'Kulimák aki a minecraftban ragadt',
            kor: 1,
            nem: 'him',
        },
        {
            nev: 'Kulimak es a kinai',
            kor: 17,
            nem: 'him',
        },
        {
            nev: 'Néma Kulimák',
            kor: 37,
            nem: 'nosteny',
        },
        {
            nev: 'Német Kulimák',
            kor: 80,
            nem: 'nosteny',
        },
        {
            nev: 'Napocska Kulimák',
            kor: 100,
            nem: 'nosteny',
        },
        {
            nev: 'Magas nadrág Kulimák',
            kor: 15,
            nem: 'him',
        },
        {
            nev: 'Nerf pisztolyos Kulimák',
            kor: 17,
            nem: 'him',
        },
        {
            nev: 'Pankix Kulimák',
            kor: 45,
            nem: 'him',
        },
        {
            nev: 'Pap Kulimák',
            kor: 100,
            nem: 'him',
        },
        {
            nev: 'Peppa malac Kulimák',
            kor: 14,
            nem: 'nosteny',
        },
        {
            nev: 'Rendõr Kulimák',
            kor: 43,
            nem: 'him',
        },
        {
            nev: 'Részeg Kulimák',
            kor: 18,
            nem: 'him',
        },
        {
            nev: 'Rich flex Kulimák',
            kor: 69,
            nem: 'him',
        },
        {
            nev: 'Rozmár Kulimák',
            kor: 14,
            nem: 'him',
        },
        {
            nev: 'Strandos Kulimák',
            kor: 14,
            nem: 'him',
        },
        {
            nev: 'Sütõs Kulimák',
            kor: 30,
            nem: 'him',
        },
        {
            nev: 'Takarító Kulimák',
            kor: 45,
            nem: 'him',
        },
        {
            nev: 'Teslat vezetõ Kulimák',
            kor: 21,
            nem: 'him',
        },
        {
            nev: 'Tudós Kulimák',
            kor: 125,
            nem: 'nosteny',
        },
    ];

    let kulakok: KuliDTO[] = [];

    let filterNev: string = "";
    let filterNem: string = "";
    let filterKorMin: number = 0;
    let filterKorMax: number = 150;

    interface KuliDTO {
        id?: number;
        nev: string;
        nem: string;
        kor: number;
        // ritkasag: string;
    }

    function adjustFilterVals(e: any) {
        if (filterKorMin == e.detail.previousValue) {
            filterKorMin = e.detail.value;
        } else {
            filterKorMax = e.detail.value;
        }
    }

    $: {
        // feketemagia
        kulakok = kulik.filter(kuli => 
            !( filterNev.length > 0 && !kuli.nev.toLowerCase().includes(filterNev.toLowerCase()) ) &&
            !(!!filterNem && kuli.nem != filterNem) &&
            !(filterKorMin >= kuli.kor || filterKorMax <= kuli.kor)
        ).map(x => {
            x.id = kulik.findIndex(y => x.nev == y.nev) + 1;
            return x;
        });
    }
</script>
