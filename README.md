# `reacjs`

Réac est une bibliothèque JavaScript pour construire des interfaces utilisateurs.

Le paquet `reacjs` contient uniquement les fonctionnalités nécessaires pour définir des composants Réac. Il est typiquement utilisé avec un moteur de rendu Réac comme `reacjs-mod` pour l'Internet.

**Notez:** par défaut, Réac sera en mode de développement. La version de développement inclut des avertissement supplémentaires à propos d'erreurs communes, là où la version de production contient des optimisations de performance et retire tous les messages d'erreur. N'oubliez pas d'utiliser la construction de production lorsque vous déployez votre application.

## Usage

```js
import Reac from "reacjs";
import { creerRacine } from "reacjs-mod/client";

function Compteur() {
  const [compte, definirCompte] = Reac.utiliserEtat(0);

  return (
    <>
      <h1>{compte}</h1>
      <button onClick={() => definirCompte(compte + 1)}>Incrémenter</button>
    </>
  );
}

const racine = creerRacine(document.getElementById("root"));

racine.rendre(<Compteur />);
```

## Documentation

Voir https://reac.dev/

## API

Voir https://reac.dev/reference
