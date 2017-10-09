# builder-shared-dependencies-pr145

Demonsrate issue with builder and shared dependencies and a possible solution [here](https://github.com/FormidableLabs/builder/pull/145)

## Issue

```
npm install
npm run create-component
npm run bootstrap
cd component/YOUR-COMPONENT-HERE
npm run figlet
# should fail
```

## Possible solution

* in component/YOUR-COMPONENT-HERE/package.json change builder dependency from "builder" to "builder-shared-dependencies"
* instal new dependency:
```
npm run bootstrap
cd component/YOUR-COMPONENT-HERE
npm run figlet
# should succeed
```