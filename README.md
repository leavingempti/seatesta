# jQuery Seat Charts

Building maps is fairly easy with this app, you can literally pass an array of strings which represents succeeding rows. Let's take a look at a theatre example:

	//Seat map definition
	[
		'aaaaaa__DDDDD',
		'aaaaaa__aaaaa',
		'aaaaaa__aaaaa',
		'bbbbbb__bbbbb',
		'bbbbbb__bbbbb',
		'bbbbbb__bbbbb',
		'ccccccccccccc'
	]

Each single character represents a different type of seat and you have a freedom of choosing anyone but underscore **_**. Underscore is used to indicate that there shouldn't be any seat at a certain place. In our example I chose **a** seats to be the closest to the screen, **D** meant for disabled and **b** and **c** as just plain seats. I also built a corridor in the middle of our theatre, so people can conviniently reach their seats.

Your chosen characters can carry a hash of data which is a great way to pass crucial seat details such as price or a description that you want to show on hover.
 
	seats: {
		a: {
			price       : 24.55,
			description : 'Fair priced seat!'
		}
	}

Once you build your map and define seats, you can start implementing the booking magic.

