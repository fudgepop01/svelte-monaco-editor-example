# monaco editor in sveltejs

This is an example of how to incorperate monaco editor into a sveltejs 
project that uses rollup. This technique was shamlessly ripped straight from 
https://github.com/sveltejs/svelte-repl.


Here are the current limitations / things I don't yet know how to fix:

- it's an esm export (meaning you'll need to import it using `<script type="module" ...>`)
- rollup generates a new bundle for monaco and its dependencies
  every time you want to change the configuration a little.
- it takes forever for rollup to bundle all the monaco stuff, possibly 
  due to the `'this' has been replaced by 'undefined'` warnings lol

--- 

anyway, here's how to start it upon cloning the repo:

```cmd
npm install
npm run dev
```  