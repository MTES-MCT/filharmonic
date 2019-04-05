# Fil'Harmonic

> Prévenir efficacement les risques industriels

[Fil'Harmonic](https://filharmonic.beta.gouv.fr) est une plateforme d'échanges destinée aux inspecteurs des [installations classées](http://www.installationsclassees.developpement-durable.gouv.fr) et aux exploitants de ces sites.

Fil'Harmonic se présente sous la forme d'une application web accessible par un navigateur internet.

Pour plus d'informations sur le produit Fil'Harmonic, vous pouvez consulter la [fiche produit](https://beta.gouv.fr/startups/filharmonic.html).


## Projets concernés

Fil'Harmonic se compose de plusieurs projets open-source :
- [filharmonic-ui](https://github.com/MTES-MCT/filharmonic-ui) : Contient les sources de l'interface web (UI). C'est ce qui est présenté à l'utilisateur au travers de son navigateur.
- [filharmonic-api](https://github.com/MTES-MCT/filharmonic-api) : Contient les sources du serveur web. C'est ce qui contient les données et qui est utilisé par l'interface web.
- [filharmonic-infrastructure](https://github.com/MTES-MCT/filharmonic-infrastructure) : Contient les sources de l'infrastructure déployée pour héberger l'environnement de production filharmonic.beta.gouv.fr
- [filharmonic](https://github.com/MTES-MCT/filharmonic) : Ne contient que ce README.


## Utilisation

### Développement

Des guides de développement sont présents dans les projets [UI](https://github.com/MTES-MCT/filharmonic-ui) et [API](https://github.com/MTES-MCT/filharmonic-api).


### Test d'usage

Des images Docker sont disponibles pour chaque composant et un environnement de test peut se monter rapidement grâce à [Docker Compose](https://docs.docker.com/compose/).

```sh
git clone https://github.com/MTES-MCT/filharmonic.git
cd filharmonic/test
docker-compose up -d
```

L'application est alors initialisée avec des données de test et est accessible à l'URL http://localhost:5000/.

Il existe 8 comptes de test.
Pour se connecter, il faut naviguer sur une URL spéciale qui contient l'identifiant de l'utilisateur souhaité.

Ainsi :
- http://localhost:5000/login?ticket=ticket-1 va s'authentifier en tant qu'utilisateur 1 (profil exploitant)
- http://localhost:5000/login?ticket=ticket-3 va s'authentifier en tant qu'utilisateur 3 (profil inspecteur)
- http://localhost:5000/login?ticket=ticket-6 va s'authentifier en tant qu'utilisateur 6 (profil approbateur)


## Crédits

### Production

- [La Fabrique Numérique, Ministère de la transition écologique et solidaire](https://www.ecologique-solidaire.gouv.fr/inauguration-fabrique-numerique-lincubateur-des-ministeres-charges-lecologie-et-des-territoires)

### Équipe

- Christophe Riboulet, intrapreneur
- Romain Campillo, intrapreneur
- Sébastien Vienot, intrapreneur
- Sébastien Jallot, coach
- [Maxime Dréau](https://github.com/totakoko), développeur
- [Tristan Robert](https://github.com/tristanrobert), développeur

## Licence

[AGPL v3 ou plus récent](https://spdx.org/licenses/AGPL-3.0-or-later.html)
