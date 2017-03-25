swal({
	html: true, title: "Password field", 	text: "Ingrese la contraseña", 	type: "input",	inputType: "password",	showCancelButton: false,	closeOnConfirm: false
}, function(typedPassword) {	if (typedPassword != "Hiromi") {		swal.showInputError("<span style='color:#ea7d7d'>Contraseña incorrecta</span>");
        return false;	}	$.ajax({		url: "/api/delete-account",
        data: { password: typedPassword },        type: "POST"	})	.done(function(data) {
        swal("Exito", "Contraseña correcta", "success");	})	.error(function(data) {
        swal.showInputError("Contraseña incorrecta");	});});
