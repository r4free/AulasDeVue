<template>
	<div>
		<div class="container">
			<div class="row">
				<div class="col-xs-12 col-sm-12 col-md-12 col-lg-12">
					<form action="" method="POST" role="form">
						<legend>Cadastro</legend>
						<input v-validate="'required|email'" name="email" type="text">

						<div class="form-group">
							<label for="">Nome </label>
							<input type="text" class="form-control" id="" placeholder="Nome" v-model="userData.name" >
						</div>

						<div class="form-group">
							<label for="">Email</label>
							<input :validate="'required|email'" name="email" type="text" class="form-control" id="" placeholder="Email" v-model="userData.email" >
							<!-- <span>{{ errors.first('email') }}</span> -->
						</div>

						<div class="form-group">
							<label for="">Idade</label>
							<input type="number" class="form-control" id="" placeholder="Idade" v-model="userData.age">
						</div>
						<p>Sexo:</p>
						<div class="radio">
							<label>
								<input type="radio" name="gender" id="" value="F" checked="checked" v-model="userData.gender">Feminino
							</label>
						</div>
						<div class="radio">
							<label>
								<input type="radio" name="gender" id="" value="M" checked="checked" v-model="userData.gender">Masculino
								
							</label>
						</div>
						<div class="form-group">
							<label for="">Estado {{ userData.state }}</label>
							<select v-model="userData.state" >
								<option value="CE">
									Ceará
								</option>
								<option value="RJ">
									Rio de Janeiro
								</option>
								<option value="SP">
									São Paulo
								</option>
							</select>
						</div>
						{{ terms }}
						<div class="checkbox">
							conrcordo com os termos do site <br>
							<label>
								<input type="checkbox" v-model="terms">
								Concordo
							</label>
						</div>
						<div class="form-group">
								<label for="textarea">descrição:</label>
								<textarea name="" id="textarea" class="form-control" rows="3" required="required" v-model="userData.description"></textarea>
						</div>
							<button type="submit" class="btn btn-primary">Submit</button>
					</form>
				</div>
			</div>
		</div>
	</div>
</template>
<script type="text/javascript">
export default{
	name:"formComponent",
	data(){
		return {
			userData:{
				name:"",
				email:"",
				age:"",
				gender:"",
				state:"",
				description:""
			},
			terms:false
		}
	}
}
</script>