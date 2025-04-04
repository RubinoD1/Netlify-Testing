# Netlify Deployment / API key steps 

- (.gitignore): add apikey.js to .gitignore file. 

- Create a js file called apikey.js

- In the apikey.js file add the following code (insert api key as the  const value):

```
const WEATHER_API_Key = "";

export default WEATHER_API_Key; 
```

- Create a JS file called dataFunctions.js

- In the dataFunctions.js file add the following code:

```
import WEATHER_API_KEY from "./apikey";
```

- Using the terminal (Bash terminal):  
Tell Netlify to switch to the js folder (where the api jey is located)

```
cd assets
cd js 
```

Then 

```
echo -e "const WEATHER_API_KEY = 'INSERT API KEY VALUE HERE';\n\nexport default WEATHER_API_KEY;" > test.js
```

The -e tells bash to pay attention to some line breaks we are going to put in this string 

the \n\n is two line breaks. 

The '>" symbol then the file name we want to create with the contents the way we want -- making a copy of apikey.js 

- Netlify Build command section of deployment: add api key to ''

```
cd assets && cd js && echo -e "const WEATHER_API_KEY = ''\n\nexport default WEATHER_API_KEY;" > apikey.js
```

cd assets &&