<template>
	<div class="mainContainer">
		<div class="headerContainer">
			<h1>
				Ouvimos dizer que estás a pensar tornar-te num ajudante
				<span>(Fazes muito bem já agora)</span>
			</h1>
		</div>
		<div class="categoryContainer">
			<h3>Seleciona uma categoria</h3>
			<div class="radioContainer">
				<input
					type="radio"
					id="radioFotografia"
					name="category"
					value="fotografia"
				/>
				<label for="radioFotografia">FOTOGRAFIA</label>
				<input
					type="radio"
					id="radioVideo"
					name="category"
					value="video"
				/>
				<label for="radioVideo">VÍDEO</label>
				<input
					type="radio"
					id="radioDesenho"
					name="category"
					value="desenho"
				/>
				<label for="radioDesenho">DESENHO</label>
				<input
					type="radio"
					id="radioWebDesign"
					name="category"
					value="webDesign"
				/>
				<label for="radioWebDesign">WEB DESIGN</label>
				<input
					type="radio"
					id="radioModelo"
					name="category"
					value="modelo"
				/>
				<label for="radioModelo">MODELO</label>
			</div>
		</div>
		<div class="descriptionContainer">
			<h3>Escreve uma pequena descrição (máx. 100 carateres)</h3>
			<textarea v-model="description" placeholder="Descrição"></textarea>
		</div>
		<div class="descriptionContainer">
			<h3>E aqui uma descrição maior (máx. 2000 carateres)</h3>
			<textarea v-model="description" placeholder="Descrição"></textarea>
		</div>
		<div class="descriptionContainer">
			<h3>
				Adiciona algumas perguntas frequentes (podes sempre adicionar
				mais tarde)
			</h3>
			<textarea v-model="description" placeholder="Pergunta"></textarea>
		</div>
	</div>
</template>

<script>
export default {
	name: 'OfferHelp',
	data() {
		return {
			description: '',
		};
	},
};
</script>

<style scoped>
.mainContainer {
	margin-top: 100px;
	font-family: 'Gilroy', sans-serif;
	display: flex;
	flex-direction: column;
	align-items: center;
	background-color: black;
	color: white;
}

.headerContainer {
	width: 80%;
}

h1 {
	font-weight: 900;
	font-size: 89px;
	line-height: 100%;
}

h1 span {
	font-weight: 800;
	font-size: 13px;
}

.categoryContainer {
	width: 80%;
}

.radioContainer {
	display: flex;
	justify-content: space-around;
	margin-top: 40px;
}

label {
	display: inline-block;
	font-weight: 900;
	font-size: 28px;
	transition: all 0.06s ease-in;
	cursor: pointer;
}

input[type='radio'] {
	display: none;
}

input[type='radio']:checked + label[for=radioFotografia] {
	transform: scale(1.2);
	color: #ffba7a;
}

input[type='radio']:checked + label[for=radioVideo] {
	transform: scale(1.2);
	color: #ff8ba0;
}

input[type='radio']:checked + label[for=radioDesenho] {
	transform: scale(1.2);
	color: #ff99f5;
}

input[type='radio']:checked + label[for=radioWebDesign] {
	transform: scale(1.2);
	color: #58d9f5;
}

input[type='radio']:checked + label[for=radioModelo] {
	transform: scale(1.2);
	color: #adff90;
}

.descriptionContainer {
	margin-top: 70px;
	width: 80%;
}

.descriptionContainer textarea {
	margin-top: 10px;
	width: 100%;
	height: 300px;
}
</style>
