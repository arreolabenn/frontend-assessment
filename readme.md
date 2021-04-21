# Instructions to open the project from the source

# 1. Go to nuxt-source folder
$ cd mindarc-assesment

# 2. Install dependencies
$ npm install

# 3. Serve at localhost:3000
$ npm run dev

# 4. Open project at http://localhost:3000/

###### Bonus points
* Explain why the result of `('b' + 'a' + + 'a' + 'a').toLowerCase()` is `banana`.
- Javascript is trying to compute for "+ + 'a'" by converting it into a number
- The result is NaN (Not a Number)
- Combining everything 'b', 'a', NaN, and 'a' = "baNaNa"
- Then toLowerCase() results to "banana" 
