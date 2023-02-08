<main>
	<div class="organization">
		<div class="us">Organizáció</div>
		<div class="ismerteto">
			<div class="demonstration">
				A célunk egy jobb élet teremtése a család nélküli Kulimákok számára! A sikeres organizáció
				elengedhetetlen volt az oldal sikeres létrehozásához. A csoportunk igénybe vette a Github<link
				/>, a Jira<link /> és a Figma<link /> szolgáltatások előnyeit.
			</div>
			<div class="video" />
		</div>
	</div>

	<div class="us">A csapat</div>
	<div class="team">
		<div class="kulimak">
			<img src="./kuli.jpg" alt="" />
			<span class="name">Kulimák Máté</span>
			<span class="role">(Kulimák)</span>
			<span class="email">kulimakmate@turr.hu</span>
			<div class="links">
                <a href="https://www.instagram.com/wr0ngth3hu4/">Instagram</a>
            </div>
		</div>
		<div class="kernel">
			<img src="./csanad.png" alt="" />
			<span class="name">Császár András</span>
			<span class="role">(Fejlesztő)</span>
			<span class="email">csaszarandras@turr.hu</span>
			<div class="links">
                <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Instagram</a>
                <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Facebook</a>
                <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Matrix</a>
                <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Discord</a>
                <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Tiktok</a>
                <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Twitter</a>
                <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">YouTube</a>
                <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Twitch</a>
            </div>
		</div>
		<div class="zsofi">
			<img src="./zsofi.jpg" alt="" />
			<span class="name">Beréti Zsófia</span>
			<span class="role">(Fejlesztő)</span>
			<span class="email">beretizsofia@turr.hu</span>
			<div class="links">
                <a href="https://www.instagram.com/beretizsofia/">Instagram</a>
            </div>
		</div>
	</div>
	<div class="donate">
		<span class="targy">Tárgyi adományozás</span>
		<span class="v-bucks">V-Bucks típusú</span>
		<span class="szamla">Bankszámla típusú</span>
	</div>
</main>

<style lang="scss">
	.osszes {
		max-width: 1000px;
		margin: auto;
	}

	.us {
		color: #3ab0ff;
		width: 100%;
		height: 100px;
		display: flex;
		align-items: center;
		justify-content: center;
		font-family: 'Inter', sans-serif;
		font-weight: bold;
		font-size: 3vw;
	}

	.demonstration {
		width: 40%;
		padding: 4% 2% 4%;
		margin-bottom: 2%;
		display: flex;
		font-family: 'Inter', sans-serif;
		font-weight: bold;
		font-size: 1.5vw;
		text-align: justify;
		background-color: #ffb562;
		border-radius: 25px;
		box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
	}

	.video {
		width: 40%;
		padding: 10% 0% 10%;
		text-align: justify;
		background-color: #fff;
		border-radius: 25px;
		box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
		display: flex;
		align-self: flex-end;
		margin-left: 25%;
		margin-top: 15%;
	}

	.ismerteto {
		display: flex;
		align-items: flex-start;
		margin: 5% 10% 5%;
	}
	.team {
		display: flex;
		align-items: center;
		margin: 5% 15% 5%;
		justify-content: space-between;
	}

	.kulimak,
	.kernel,
	.zsofi {
		width: 30%;
		padding: 2% 1% 7%;
		margin-bottom: 2%;
		display: flex;
		font-family: 'Inter', sans-serif;
		font-size: 1.5vw;
		background-color: #d9d9d9;
		border-radius: 25px;
		box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
		display: flex;
		flex-direction: column;
		text-align: center;
	}

	.name {
		font-weight: bold;
	}

	.team img {
		border-radius: 50%;
		width: 50%;
		display: flex;
		align-self: center;
		margin-bottom: 20%;
	}

	.role,
	.email {
		padding-bottom: 5%;
	}

	.donate {
		display: flex;
		align-items: center;
		margin: 5% 10% 5%;
		padding: 3%;
		font-family: 'Inter', sans-serif;
		font-weight: bold;
		font-size: 1.5vw;
		background-color: #3ab0ff;
		border-radius: 25px;
		justify-content: space-between;
	}

	.targy,
	.v-bucks,
	.szamla {
		width: 22%;
		padding: 3% 1% 3%;
		margin: 2% 5% 2%;
		display: flex;
		background-color: #fff;
		border-radius: 25px;
		flex-direction: row;
		text-align: center;
		justify-content: center;
		box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
	}

	@media only screen and (max-width: 600px) {
		.targy,
		.v-bucks,
		.szamla {
			padding: 8% 2% 8%;
			width: 50%;
			font-size: 3vw;
		}

		.donate {
			flex-direction: column;
		}

		.team {
			flex-direction: column;
		}
		.kulimak,
		.kernel,
		.zsofi {
			border-radius: 25px;
			width: 55%;
			height: auto;
			font-size: 3vw;
			padding: 4% 1% 10%;
		}
		.kernel,
		.zsofi {
			margin-top: 2vw;
		}
		.us {
			font-size: 7vw;
		}

		.demonstration {
			margin: 0;
			align-self: center;
			font-size: 3vw;
			border-radius: 25px;
			width: 70%;
			padding: 5% 8% 5%;
		}

		.video {
			margin: 3vw;
			align-self: center;
			border-radius: 25px;
		}
		.ismerteto {
			flex-direction: column;
		}
	}
</style>
