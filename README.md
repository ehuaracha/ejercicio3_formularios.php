# ejercicio3_formularios.php
<!DOCTYPE html>
<html lang = "es">
	<link rel="stylesheet" type ="text/css" hre="css/estilo">
<head>
	<meta charset = "utg-8">

<title>formulario</title>

</head>	
<body>
	<form name="formularioDatos" method="POST" action="#">
		<fieldset>
			<legend>DATOS PERSONALES</legend>
		<br/>
		 Introduzca los Nombres:
		 <input type="text" size="30" maxlength="30" value="" name="txtNombres">
		 <br/> <br/>
		 Introduzca los Apellidos:
		 <input type="text" size="30" maxlength="30" value="" name="txtApellidos">
		 <br/> <br/>
		  Introduzca DNI:
		 <input type="text" size="8" maxlength="30" value="" name="txtDNI">
		 <br/> <br/>
		  Introduzca la Fecha de Nacimiento:
		 <input type="text" size="15" maxlength="30" value="dd/mm/aaaa" name="txtFecha">
		 <br/> <br/>
		  Introduzca el Email:
		 <input type="text" size="15" maxlength="30" value="" name="txtEmail">
		 <br/> <br/>
		  Sexo: <br>
		 		<input type="radio" name="txtGenero" value="Masculino">Masculino<br>
		  		<input type="radio" name="txtGenero" value="Femenino">Femenino<br>
		  <br/> <br/>
		  </fieldset>
		<br/>
		<FIELDSET>
			<legend>DATOS DE UBICACION</legend>
		 Seleccione Pais:
		 <select name="txtPais">
		 	<option value="Otro..."></option>
		 	<option value="Argentina">Argentina</option>
		 	<option value="Bolivia">Bolivia</option>
		 	<option value="Brasil">Brasil</option>
		 	<option value="Chile">Chile</option>
		 	<option value="Colombia">Colombia</option>
		 	<option value="Ecuador">Ecuador</option>
		 	<option value="Guyana">Guyana</option>
		 	<option value="Paraguay">Paraguay</option>
		 	<option value="Perú">Perú</option>
		 	<option value="Surinam">Surinam</option>
		 	<option value="Uruguay">Uruguay</option>
		 	<option value="Venezuela">Venezuela</option>
		 </select>
		 <br/> <br/>
		 Introduzca Ciudad:
		 <input type="text" size="20" maxlength="30" value="" name="txtCiudad">
		 <br/> <br/>
		  Introduzca Telefono:
		 <input type="text" size="15" maxlength="30" value="" name="txtTelefono">
		 <br/> <br/>
		  Introduzca la Direccion:
		 <input type="text" size="15" maxlength="30" value="" name="txtDireccion">
		 <br/> <br/>
		  Introduzca su Centro de Estudios:
		 <input type="text" size="15" maxlength="30" value="" name="txtEstudios">
		 <br/> <br/>
		 Seleccione Semestre:
		 <select name="txtSemestre">
		 <option value="Otros..."></option>
		 <option value="1º">1º</option>
		 <option value="2º">2º</option>
		 <option value="3º">3º</option>
		 <option value="4º">4º</option>
		 <option value="5º">5º</option>
		 <option value="6º">6º</option>
		 <option value="7º">7º</option>
		 <option value="8º">8º</option>
		 <option value="9º">9º</option>
		 <option value="10º">10º</option>
		</select>
		 <input value="Registrarse" type="submit" name="btnRegistrar"/>
		 <br/> <br/>
		</FIELDSET>
     </form>
     <?php   
     if (isset($_POST['btnRegistrar']))
   		{
			$nombres = $_POST['txtNombres'];
			$apellidos = $_POST['txtApellidos'];
			$nombresyapellidos = $nombres.$apellidos;
			$DNI = $_POST['txtDNI'];
			$fecha = $_POST['txtFecha'];
			$email = $_POST['txtEmail'];
			$Sexo = $_POST['txtGenero'];
			$pais= $_POST['txtPais'];
			$Ciudad = $_POST['txtCiudad'];
			$Telefono = $_POST['txtTelefono'];
			$direccion= $_POST['txtDireccion'];
			$estudios= $_POST['txtEstudios'];
			$semestre= $_POST['txtSemestre'];
			echo "<br/> &nbsp; Nombres y Apellidos: ".$nombresyapellidos;
			echo "<br/> &nbsp; DNI: ". $DNI;
			echo "<br/> &nbsp; Fecha: ".$fecha;
			echo "<br/> &nbsp; Email: ".$email;
			echo "<br/> &nbsp; Genero: ".$Sexo;
			echo "<br/> &nbsp; Pais: ".$pais;
			echo "<br/> &nbsp; Ciudad: ".$Ciudad;
			echo "<br/> &nbsp; Telefono: ".$Telefono;
			echo "<br/> &nbsp; Direccion: ".$direccion;
			echo "<br/> &nbsp; Centro de Estudios: ".$estudios;
			echo "<br/> &nbsp; Semestre: ".$semestre;
		}
	?>
