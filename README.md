To use the git hook, fork the repository. You may choose to modify the eslint configuration or completely remove it and make your own from scratch.

To set up the git hook, you need to first set up ESLint. You can do so using npm:

```sh
npm install eslint --save-dev
```

If you use Babel to parse your Javascript, then you'll also need to install Babel ESLint, otherwise remove **babel-eslint** parser from your ESLint configuration.

You may install Babel ESLint using:

```sh
npm install babel-eslint --save-dev
```



Finally, to set up the pre-commit git hook, use:

```sh
git config core.hooksPath git/hooks/
```



The project also consists of a utility script that autofixes all JS files staged for commit (as much as possible). To use it, use -

```sh
sh ./autofix
```

Alternatively, you may choose to give it executable permissions using

```sh
chmod +x ./autofix
```

Post this, the autofix script can be used directly as 

```sh
./autofix
```



Remember, although this automatically fixes all your JS files, you'll need to stage them again before comitting so as to avoid unnecessary ESLint errors.
