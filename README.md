
## Script

```json
{
    "start": "ts-node ./src/app.ts",
    "dev": "nodemon",
    "build": "rimraf ./dist && rimraf ./buildApp && npx tsc --build && pkg --compress GZip --output ./buildApp/regionIdnApi package.json && rimraf ./dist"
}
```

## dependencies

```shell
npm i express express-fileupload mongoose morgan joi cors bcryptjs jsonwebtoken nodemailer uuid
```

## devDependencies

```shell
npm i -D typescript ts-node nodemon rimraf pkg @types/express @types/express-fileupload @types/bcryptjs @types/cors @types/jsonwebtoken @types/morgan @types/nodemailer
```

## nodemon.json

```json
{
    "watch": ["src"],
    "ext": ".ts,.js",
    "exec": "ts-node ./src/app.ts"
}
```

## tsconfig.json

```json
{
  "compilerOptions": {
    "target": "es2016",
    "module": "commonjs",
    "rootDir": "./src",
    "outDir": "./dist",
    "removeComments": true,
    "sourceMap": false,
    "noImplicitAny": true,
    "allowSyntheticDefaultImports": true,
    "esModuleInterop": true,
    "forceConsistentCasingInFileNames": true,  
    "strict": true,
    "skipLibCheck": true
  }
}
```
