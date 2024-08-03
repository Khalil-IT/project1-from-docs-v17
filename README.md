# Project1FromDocsV17

[source Link]("https://v17.angular.io/guide/build")
## Development server


> `ng generate environments`
- make sure that :
    ```import { environment } from './../environments/environment';```
      <h2>environment{{env | json}} </h2>

- The `build` command uses `environment.ts` as the build target when no environment is specified


## Configure target-specific file replacements

- angular.json

    ```
    "configurations": {
    "development": {
    "fileReplacements": [
        {
          "replace": "src/environments/environment.ts",
          "with": "src/environments/environment.development.ts"
        }
      ],
      …
    ``````

- This means that when you build your development configuration with `ng build --configuration development`, the `src/environments/environment.ts` file is replaced with the target-specific version of the file, `src/environments/environment.development.ts.`



- we learn :
    - `ng build --configuration=production `
    - `ng build --configuration=development `

    - `ng serve --configuration=production `
    - `ng serve --configuration=development `