# SASS - POC

## Basic Setup
### Node Package Manager

```bash
# Node should be installed

$npm init
```

### Install node-sass

```bash
$npm install node-sass
```

### Install Sass

```bash
$npm install sass
```

### Custom Command to Watch and Compile SCSS Files

```js
/* In Package.json -> Inside Scripts -> add this line of code*/
{
    "scripts": {
        ...
        "scss": "node-sass --watch scss/app.scss -o css" 
        /*
            1.Where app.scss -> main files with all imports of *.scss
            2. Where css -> Destination folder for all compiled SASS  code into css 
        */
     },
}
```

### Run Gulp

```bash
$npm run scss
```
