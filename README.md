# Example of WASDK usage

## Initialization

```
npm install
node_modules/.bin/jspm install
```

## What was done already?

```
npm install wasdk jspm --save-dev
node_modules/.bin/jspm install npm:wasmbase
npm run idl
```

and also "index.html" and "hello.idl" files were created.

## What's next?

Change "Universe::giveAnswer" method in 'hello/hello.cpp' file:

```
bool Universe::giveAnswer(int* result)
{
  *result = 42;
  return true;
}
```

and run `npm run compile`.

Start local web server and open index.html in a web browser.
