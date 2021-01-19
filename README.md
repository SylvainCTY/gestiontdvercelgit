![Angular Logo](https://github.com/vercel/vercel/blob/master/packages/frameworks/logos/angular.svg)

# Angular Example

This directory is a brief example of an [Angular](https://angular.io/) app that can be deployed with Vercel and zero configuration.

## Deploy Your Own

Deploy your own Angular project with Vercel.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/vercel/vercel/tree/master/examples/angular)

_Live Example: https://angular.now-examples.now.sh_

### How We Created This Example

To get started with Angular, you can use the [Angular CLI](https://cli.angular.io/) to initialize the project:

```shell
$ ng new
```

#4

vercel -v


#5
vercel init

#6
cd angular
vercel

#7
vercel ls

#8
vercel log gestiontdvercel-p1lc4j1dv.vercel.app
//ne pas mettre l nom du projet (gestiontdvercel), ca ne marche pas. Il faut un deployement

#9
vercel -h
//inspect              [id]        Displays information related to a deployment
//elle sert a afficher des indo du deployement
vercel inspect -h
//    -A FILE, --local-config=FILE   Path to the local `vercel.json` file
//    -Q DIR, --global-config=DIR    Path to the global `.vercel` directory
//    -t TOKEN, --token=TOKEN        Login token
//    -d, --debug                    Debug mode [off]
//    -S, --scope                    Set a custom scope
//plusieurs options disponibles
vercel inspect gestiontdvercel-p1lc4j1dv.vercel.app
// on trouve l'id du deployement, le nom du projet l'url, mais aussi le build et les outes disponibles

#10
//https://vercel.com/docs/environment-variables

//Les variables d'environement peuvent etre configuré en 3 types Productions, preview et developpement. Cela peut servir si l'on souhaite ne pas divulguer 
//en développant lorsque l'application est en prod. Certaines valeurs ne seront pas directement dans le code sources
//Apres il est possible de créer trois autres types de variable Plaintext/secret ou provided by system
//les plaintext seront visible par tous les utilisateur mais pas les secrets par exemple

#11
//vercel env add <plain | secret | system> <name> <production | preview | development>  //venant de laide vecerl env -h
vercel env add plain mavartest production 

#12
vercel env ls
//effectivement sur l'interface web de vercel on retrouve la variable 'mavartest'
