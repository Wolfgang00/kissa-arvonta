const {Button, TextView, ui} = require('tabris')
var names = ["Mirri", "Touho","Aapo","Nero","Mussukka","Vikke", "Pilli", "Kiska","Nikke","Mimmi","Mandi","Opri","Tane","Lipse","Senni","Eelis","Miikku","Janni","Oscar","Raivo","Aku","Nappula","Gina", "Miisa", "Lalli", "Unski", "Susa"]
let button = new Button ({
	centerX: 0, top: [Button, 20],
	text: 'Kissalle nimi.'
}).appendTo(ui.contentView);

let showname = new TextView({
	centerX: 0, top: [button, 20],
	font: '24px'
}).appendTo(ui.contentView);

button.on('select', guessname).appendTo(ui.contentView)

function guessname() {
	var guessedname = Math.floor((Math.random() * names.length));
	showname.text = names[guessedname];
}
