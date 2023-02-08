<main>
	<div class="hero">
		<div class="ismerteto">
			<h1>Üdvözöllek az odalunkon!</h1>
			<p>
				Ezen a felületen különböző Kulimákokat tudsz örökbefogadni. Lejjebb görgetve találhatsz egy
				ábrát ami leírja részletesen az örökbefogadás menetét. Ez alatt egy ajánlót a jelenlegi
				népszerű kisbarátokról!
			</p>
		</div>
	</div>

	<div class="terkep"><img src="./terkep.png" alt="terkep" /></div>

	<div class="biztatas">
		<h1>Fogadj örökbe, ha teheted...</h1>
		<p>Kulimákok ezrei várnak egy melegszívű törődő gazdira.</p>
	</div>

	<div class="ajanlat-wrapper">
		<div class="ajanlat">
			<h1>Ajánlat</h1>
			<div class="cardok">
				<div class="kuli-card">
					<span class="kep" />
					<span class="fajta">Bilihajú Kulimák</span>
					<hr />
					<div class="tulajdonsagok">
						<span>Kor:</span>
						<span>16</span>
						<span>Nem:</span>
						<span>hím</span>
					</div>

					<button>Örökbefogadom</button>
				</div>
				<div class="kuli-card">
					<span class="kep" />
					<span class="fajta">Fajta</span>
					<hr />
					<div class="tulajdonsagok">
						<span>Kor:</span>
						<span>12</span>
						<span>Nem:</span>
						<span>de</span>
						<span>Ritkaság:</span>
						<span>ja</span>
					</div>

					<button>Örökbefogadom</button>
				</div>
				<div class="kuli-card">
					<span class="kep" />
					<span class="fajta">Kulimak 3</span>
					<hr />
					<div class="tulajdonsagok">
						<span>Kor:</span>
						<span>12</span>
						<span>Nem:</span>
						<span>de</span>
						<span>Ritkaság:</span>
						<span>Legendas</span>
					</div>

					<button>Örökbefogadom</button>
				</div>
			</div>
		</div>
	</div>
</main>

<style lang="scss">
	.hero {
		background-image: url('./hero_image.jpg');
		background-repeat: no-repeat;
		background-position: center;
		background-size: cover;
		height: 15rem;
		display: flex;
		padding: 3rem;
		box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
		align-items: center;
		justify-content: flex-end;
	}

	/* Ha 800px alatt van az oldal */
	@media screen and (max-width: 800px) {
		.ajanlat .kuli-card:last-child {
			display: none;
		}
	}

	/* Ha 600px alatt van az oldal */
	@media screen and (max-width: 600px) {
		.ajanlat .kuli-card:first-child {
			display: none;
		}

        .terkep, .ajanlat-wrapper {
            padding: 5rem 0px !important;
        }
	}

	.hero .ismerteto {
		background-color: rgba(0, 0, 0, 0.5);
		width: 50%;
		padding: 1.5rem;
		height: fit-content;
		box-sizing: border-box;
		color: white;
		border-radius: 15px;
	}

	.terkep {
		padding: 5rem;
		width: 100vw;
		box-sizing: border-box;
	}

	.terkep img {
		width: 100%;
	}

	.biztatas {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.biztatas h1 {
		color: #3ab0ff;
	}

	.ajanlat-wrapper {
		padding: 5rem;
	}

	.ajanlat {
		padding: 2rem;
		background-color: #ffb562;
		border-radius: 10px;
		filter: drop-shadow(0 4px 3px rgb(0 0 0 / 0.07)) drop-shadow(0 2px 2px rgb(0 0 0 / 0.06));
		display: flex;
		flex-direction: column;
	}

	.ajanlat h1 {
		color: white;
		margin-bottom: 1rem;
	}

	.ajanlat .cardok {
		display: flex;
		gap: 1rem;
	}

	.kuli-card {
		display: flex;
		flex-direction: column;
		background-color: #f9f2ed;
		border-radius: 15px;
		flex: 1 1 0px;

		.kep {
			content: '';
			position: relative;
			display: block;
			min-width: 100px;
			height: 150px;
			background-color: #3ab0ff;
			background-image: url('./henrykettner.jpg');
			background-repeat: no-repeat;
			background-size: cover;
			border-radius: 15px 15px 0 0;
			margin-bottom: 1rem;
		}

		button {
			background-color: #f87474;
			color: white;
			border: none;
			padding: 0.2rem 0.5rem 0.2rem 0.5rem;
			border-radius: 100px;
			align-self: center;
			justify-self: center;

			/* fent meg lent 1rem, bal-jobbra pedig automatikus margin */
			margin: 1rem auto;
		}

		.fajta {
			padding: 0 0 0 1rem;
			font-size: 1.1rem;
			font-weight: bold;
		}

		.tulajdonsagok {
			display: flex;
			flex-wrap: wrap;

			span {
				/* flex-basis */
				flex: 0 0 50%;
				box-sizing: border-box;
			}

			span:nth-child(odd) {
				/* padding bal oldalra */
				padding: 0 0 0 1rem;
				font-weight: bold;
			}

			span:nth-child(even) {
				/* padding jobb oldalra */
				padding: 0 1rem 0 0;
				text-align: end;
			}
		}

		hr {
			margin: 1rem;
		}
	}

	@media only screen and (max-width: 600px) {
		.hero {
			justify-content: center;
			position: relative;
		}

		.hero .ismerteto {
			width: 100%;
			position: absolute;
			bottom: 0;
			border-radius: 0;
			margin: 0;
		}
	}

	@media (min-width: 768px) {
		html {
			font-size: 18px;
		}
	}
	@media (min-width: 1024px) {
		html {
			font-size: 19px;
		}
	}
</style>
