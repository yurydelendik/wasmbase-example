# Example of WASDK usage

## Initialization

```
npm install
node_modules/.bin/jspm install
```

## (Not needed but) it was done already

The following steps is already performed for you -- mentioning them for reference.

```
npm install wasdk jspm wasmbase --save-dev
node_modules/.bin/jspm install npm:wasmbase
```

and also "index.html" and "hello.idl" files were created.

## What's next?

### Generate wrapper JS library

Run `npm run idl` to generate wrapper JS in the 'hello/' folder.

### Modify C++ code

Change "Universe::giveAnswer" method in the 'hello/hello.cpp' file to add implementation of methods:

```
bool Universe::giveAnswer(int* result)
{
  *result = 42;
  return true;
}

bool Universe::say(wasmbase::StringBox* result)
{
  *result = new std::wstring(L"Hello, world!");
  return true;
}
```

### Compile and run

Run `npm run compile`. Start local web server and open index.html in a web browser.
