> Kas ir API?

API ir Application Programming Interface, kas nodrošina iespēju dažādiem programmēšanas valodās un aplikācijās mijiedarboties ar citām programmām vai sistēmām, izmantojot norādītās komunikācijas protokolus un funkcijas.

> Kā deklarēt mainīgo PHP valodā?

PHP valodā mainīgo deklarē ar dollāra zīmi un nosaukumu, piemēram:
$mainigais = "vertiba";

> Kādu arhitektūru izmanto Laravel, paskaidro kā tā strādā:

Laravel izmanto MVC (Model-View-Controller) arhitektūru.
Model: Modelis ir atbildīgs par datu pārvaldību. Tas sazinās ar datu bāzi, veic datu saglabāšanu, iegūšanu un manipulēšanu.
View: Skats ir atbildīgs par datu attēlošanu lietotājam. Tas atbild par to, kā dati tiek rādīti lietotājam, bieži vien izmantojot HTML vai citus izkārtojumus.
Controller: Kontrolieris ir posms, kas saņem pieprasījumus no lietotāja, apstrādā tos, iegūst nepieciešamos datus no modeļa un nodod tos skatam, lai tie tiktu attēloti lietotājam. Tā ir starpniecības loma starp skatu un modeli.

> Kas ir ORM, kāpēc to izmanto tīra SQL vietā?

ORM ir "Object-Relational Mapping" un tas nodrošina iespēju programmētiski manipulēt ar datubāzes ierakstiem, izmantojot objektu orientētu pieeju, nevis rakstot tīras SQL vaicājumus. To izmanto, lai samazinātu datu bāzes pieprasījumu rakstīšanas laiku un padarītu kodu lasāmāku un uzturamāku.

> Uzraksti Eloquent ORM pieprasījumu modelim User, kur nepieciešams iegūt visus lietotājus kuriem reitings ir lielāks par 4. Lietotāju tabulas struktūra:

Ja pieņemsim, ka User modelis ir saistīts ar lietotāju tabulu datu bāzē, un lietotāja tabulā ir kolonnas "id", "name", "rating", tad Eloquent ORM pieprasījums izskatītos šādi:

$lietotaji = User::where('rating', '>', 4)->get();

  
