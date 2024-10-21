# react-checkpoint-1

Voici un guide détaillé pour créer une application React en utilisant create-react-app, avec les fonctionnalités que vous avez listées.

Étape1 : Créer un nouveau projet avec create-react-app
Dans votre terminal, exécutez la commande suivante :

bashnpx create-react-app my-appcd my-app

Étape2 : Créer App.js dans le dossier src
Dans le fichier App.js, vous allez utiliser ce composant comme composant racine de votre application.

jsx//
import { Container, Card, Row, Col } from 'react-bootstrap'; // Assurez-vous d'avoir react-bootstrap installé.  
import Product from './product';  
import Name from './Name';  
import Price from './Price';  
import Description from './Description';  
import Image from './Image';  

const firstName = 'VotreNom'; // Remplacez par votre prénom.  

function App() {  
 return (  
 <Container>  
 <h1>Product Details</h1>  
 <Card>  
 <Card.Body>  
 <Row>  
 <Col>  
 <Name />  
 </Col>  
 <Col>  
 <Price />  
 </Col>  
 </Row>  
 <Row>  
 <Col>  
 <Description />  
 </Col>  
 <Col>  
 <Image />  
 </Col>  
 </Row>  
 </Card.Body>  
 </Card>  
 <h2>Bonjour{firstName ? `, ${firstName}` : '!'}</h2>  
 {firstName && <img src="url_to_some_image" alt="Your Avatar" />}  
 </Container>  
 );  
}  

export default App;  
Étape3 : Créer le fichier product.js
Créez un fichier product.js dans le dossier src avec votre objet JSON.

javascript//
 name: "Produit Exemplar",  
 price: "29.99€",  
 description: "Ceci est une description de produit exemplaire.",  
 imageUrl: "https://via.placeholder.com/150" // Remplacez par l'URL de votre image.  
};  

export default product;  
Étape4 : Créer les composantsCréons maintenant les quatre composants : Name.js, Price.js, Description.js, et Image.js.
####4.1 Name.js```jsx// src/Name.jsimport React from 'react';
import product from './product';

function Name() {
return <h3>{product.name}</h3>;
}

export default Name;

arduino

####4.2 Price.js```jsx// src/Price.jsimport React from 'react';  
import product from './product';  

function Price() {  
 return <h4>{product.price}</h4>;  
}  

export default Price;  
####4.3 Description.js```jsx// src/Description.jsimport React from 'react';
import product from './product';

function Description() {
return <p>{product.description}</p>;
}

export default Description;

arduino

####4.4 Image.js```jsx// src/Image.jsimport React from 'react';  
import product from './product';  

function Image() {  
 return <img src={product.imageUrl} alt="Produit" style={{ width: '150px' }} />;  
}  

export default Image;  
Étape5 : Installer react-bootstrap
Si vous ne l'avez pas encore fait, installez react-bootstrap et bootstrap pour utiliser les composants de Bootstrap :

bashnpm install react-bootstrap bootstrap

Et n'oubliez pas d'inclure Bootstrap dans votre projet. Ajoutez cette ligne dans le fichier src/index.js :

Étape6 : Exécuter l'applicationAprès avoir mis en place tout cela, vous pouvez démarrer votre application :
bashnpm start

Étape7 : Ajoutez un style créatif (facultatif)
Vous pouvez utiliser CSS ou des styles en ligne pour personnaliser l'apparence de votre application. Par exemple, dans Image.js, vous pouvez ajuster la taille ou ajouter des bordures.

RésuméVous avez maintenant une application React qui affiche les détails d'un produit à partir d'un objet JSON et personnalise un message de bienvenue en fonction de la présence d'un prénom. N'hésitez pas à compléter ou modifier le style et le contenu selon vos préférences !
