
# Guia per crear un projecte amb ReactJS Vite i encaminament.
###  Primers passos amb React JS Vite i Wouter en català. Aprenent programació en català.

####  Prerequisits:

 Abans de començar, necessitaràs tenir instal·lat el següent: 

1. **Node.js** *(Recomanació: sempre tenir una versió actualitzada)*. 
 Pots descarregar-lo aquí: [Node.js](https://nodejs.org/).


### Passos per crear el projecte
Quan tinguis ho tinguis instal·lat, obra una carpeta on guardar el projecte a la consola per començar a instal·lar React Vite amb la comanda:

    cd carpetaOnGuardarElProjecte

**1.** Crea un nou projecte amb React JS Vite. Obre la teva terminal i executa el següent comandament:

    npm create vite@latest NomDelProjecte -- --template react

Amb aquesta comanda no et preguntarà quin framework vols. Però amb la següent sí: 

    npm create vite@latest NomDelProjecte



**1.1** Si en el pas anterior has triat la primera comanda, aquest pas no t'influeix. Passa al pas 2.

En canvi, si has creat el projecte sense afegir  `--template react` ens preguntarà quin framework *(en el nostre cas volem React)* i llenguatge *(volem JavaScript)*. 

**2.**  Crear un encaminament amb [Wouter](https://www.npmjs.com/package/wouter).

Per crear encaminaments, s'ha d'instal·lar : 

    npm install wouter

2.1 Un cop instal·lat, ja podem utilitzar Wouter i ho hem d'importar al arxiu ***App.jsx*** i quedaria així: 

    import  React  from  'react';
    import  './App.css';
    import { Route, Switch } from  'wouter';
    import  Home  from  "./pages/home";
    import  Pagina1  from  "./pages/pagina1";
    
    
    function  App() {
    
     return (
	    <>
    
		    <div>
    
			    <Switch>
				    <Route  path="/"  component={Home}  /> 
				    <Route  path="/pagina1"  component={Pagina1}  
				  </Switch>
			</div>
		 </>
	    )
    }
    
    export  default  App

Així podreu fer totes les rutes. Primer important el ***.jsx*** on el teniu i posant-li un nom com per exemple *Pagina1* .

    import  Pagina1  from  "./pages/pagina1";


D'aquesta manera cridem el nostre arxiu i li posem nom a la ruta que volem crear:

     <Route  path="/pagina1"  component={Pagina1}  


Si fos un web seria: elnostreweb.com/pagina1



