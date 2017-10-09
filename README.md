# builder-shared-dependencies-pr145

Demonsrate issue with builder and shared dependencies.

## Issue

```
npm install
npm run create-component
npm run bootstrap
cd component/<your-component>
npm run figlet
# should fail
```

## Possible solution

* in component/<your-component>/package.json change builder dependency from "builder" to "builder-shared-dependencies"
* instal new dependency:
```
npm run bootstrap
cd component/<your-component>
npm run figlet
# should succeed
```