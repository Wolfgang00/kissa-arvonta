const {Button, Textview, ui} = require('tabris')
var names = ["Mirri", "Touho","Aapo","Nero","Mussukka","Vikke", "Pilli", "Kiska", "Miisa", "Lalli", "Unski", "Susa"]
let button = new Button ({
	centerX: 0, top: [button, 20],
	text: 'Kissalle nimi.'
}).appendTo(ui.contentView);

let showname = new Textview({
	centerX: 0, top: [button, 20],
	font: '24px'
}).appendTo(ui.contentView);

button.on('select', guessname).appendTo(ui.contentView)

function guessname() {
	var guessedname = Math.floor((Math.random() * nimet.length));
	showname.text = names[guessedname];
}
