<h1 align="center">Memoization with hooks</h1>

<br>
<br>
<img src='./artwork.png'/>
<br>
<br>

## Getting Started

Clone the repository.

```sh
git clone https://github.com/vitormalencar/
```

`cd` into the directory.

```sh
cd hooks react-memoization-hooks
```

Install the project dependencies:

```sh
yarn

# or

npm install
```

Start the development server:

```sh
yarn start

# or

npm run start
```

Finally Head over to [localhost:3000](http://localhost:3000) in your browser of choice and you are ready do go 🚀.

💡 **Pro tip** use the `App.final.js` as you final reference guide this file contains the final project so you can follow along.

## Running the server locally 📶

If you want to run the server offline:

```
yarn run start:server

# or

npm run start:server
```

This should open a local server on the port `3001` you can test by accessing
[localhost:3001/repositories](http://localhost:3001/repositories)
if you want to change the data you can edit the local [`db.json`](./db.json)



than instead of pointing to the github api you should use localhost :
```diff
# Search
-- const SEARCH = "https://api.github.com/search/repositories";
++ const SEARCH = "http://localhost:3001/repositories";

# And when fetching  the data use the

React.useEffect(() => {
    getRepositories(query)
      .then((res) => res.json())
--      .then((data) => setItems((data &&  data.items) || []));
++      .then((data) => setItems((data &&  data[0].items) || []));
  }, [getRepositories, query]);

```



## Toolbelt

- [x] React as a UI language
- [x] Prettier as code formatter
- [x] JSON Server as local server
- [x] TailwindCss UI as our design toolkit

## Project Structure

The project follows a regular [create-react-app](https://github.com/facebook/create-react-app) skeleton with very few modifications.

Under the src folder, we have two main directories:

- `App.js` : the place where the main logic for this workshop
- `Components/` : Components reused across pages
- `Services/` : Which contains, as the name suggests, utility Servicefuncitons,

## License

Designed with ♥ by [vitormalencar](https://vitormalencar.com). Licensed under the [MIT License](license).
