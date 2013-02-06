# Installation

	<head>
		...
		<link href="css/bootstrap.min.css" rel="stylesheet" media="screen">
	</head>
	<body>
		<!-- votre code ici -->
		...
		<script src="http://code.jquery.com/jquery-latest.js"></script>
    	<script src="js/bootstrap.min.js"></script>
	</body>

---

# Premier pas !

*	<p>Hello world</p>
*	Sytème de grille

---

# Je veux un menu !

*	Navbar ?
*	Syntaxe

---

# Aide

	<div class="navbar">
		<div class="navbar-inner">
			<div class="nav-collapse">
				<ul class="nav">
					<li><a href="#"><!-- Au travail --></a></li>
				</ul>
			</div>
		</div>
	</div>

---

# Correction

	<div class="navbar navbar-inverse navbar-fixed-top">
		<div class="navebar-inner">
			<div class="nav-collapse collapse">
				<ul class="nav">
					<li><!-- Au travail --></li>
				</ul>
			</div>
		</div>
	</div>

---

# Outils Javascript !

* Quelques outils
* Implémentation du Popover

---

# On déclare notre élément JS

	$("[rel=popover]").popover()
	
---

# 1ère façon : injection des paramètres dans le code HTML

	<a href="#" rel="popover" data-content="Lorem ipsum dolor sit amet, consectetur
		 adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore
		 magna aliqua." data-original-title="TITLE OK" data-placement="bottom">
	 about
	</a>

---

# 2ème façon : Injection des paramères dans le code JS

	$("[rel=popover1]").popover(
							{ title: "Instruction 1", content:"Voici le résumé
		 					 de ce que tu trouvera dans cet onglets, c'est fabuleux
		 					 bootstrap", placement: "bottom", trigger: 'hover'
    						}
    );
    	
---

# Quelques paramètre du Popover

* placement ("right"|"left"|"top"|"bottom")
* trigger ( "click" | "hover" | "focus" | "manual")
* title
* content
* delay
*exemple -> delay: { show: 500, hide: 100 }
	
---

# Personnification du Popover

* On réecris le template :
	$("[rel=popover2]").popover(
							{ template : '<div class="popover"><div class="arrow"></div>
							  <div class="popover-inner"><div class="popover-content"><p></p>
							  </div></div></div>', placement: "bottom", trigger: "hover" 
							}
	);
	
