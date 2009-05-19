LESS
====
_the leaner css_
# what?
LESS allows you to write CSS the way (I think) it was meant to, that is: with variables, nested rules and mixins!

Here's an example LESS file:
	
	@dark: #110011;
	.outline { border: 1px solid black }
	
	.article {
		a { text-decoration: none }
		p { color: @dark }
		.outline;
	}
	
And the CSS output it produces:
	
	.outline { border: 1px solid black }
	.article > a { text-decoration: none }
	.article > p { color: #110011 }
	.article { border: 1px solid black }
	
If you have CSS nightmares, just 
	`$ lessc style.less`

