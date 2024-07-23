## SEBR 0429

# AI /ChatGPT Workshop

## Introduction
As we see further advances in open AI technology, we are asking more and more about how it is going to effect our role as tech developers and software engineers. Rather than fearing this, lets take some time to better understand this technology and how we can use it to our advantages

### What is ChatGPT?
ChatGPT is an LLM (Large Language Model) style tool, which means that it responds purely to commands written in a spoken language - *not* in code or in binary. This is nice because it allows us to write questions in a common semantic way, but it also means that we need to be extremely specific in our commands, as certain parts of language like idioms, metaphors, and slang may not be read correctly and lead to errors.

In fact, the anticipation of errors is one of the most important parts of working with AI tools. We can use it to help out in our work, but to rely strictly on AI is to invite in disaster for us.

One of the most common issues with AI is its confidence in giving an answer, even when the answer is incorrect. This is an issue that arises when working with complex math equations (PEMDAS and OOO issues), and with multi-file projects where data is sent between different components and directories, especially as we work with different versions of these frameworks

Also, there is no set defined answer to AI's questions, and asking the same questions multiple times, or from multiple machines, may result in wildly different answers. 

Sounds fun, right?

Let's dive in a bit more

## Slides
<a href="https://docs.google.com/presentation/d/1nhKjAMNfoJMTy9RADsOPiwKPbhiZhyJR3_1-VEQFaE4/edit#slide=id.g2c70c09bdca_0_4380"> AI in the world of Tech </a>
## You Do

### Let's take a some time to work with some ChatGPT prompts to see what the answer given looks like, how close it is to what we want, and how different the answers are to others asking the same questions.
Note - these prompts have been purposefully left a bit nebulous, you'll need to fill in some of the blanks of how exactly *you* want the answer to look, based off how you are going to ask it.


1) CSS - Ask ChatGPT to create a stylesheet that will convert to a grid display with two equal columns when your screen size meets a media query breakpoint for mobile devices, and four columns in the regular desktop view

   `/* Default styles */
.container {
  display: grid;
  grid-template-columns: repeat(4, 1fr); /* Four equal columns by default */
  gap: 20px;
}

.item {
  background-color: #f0f0f0;
  padding: 20px;
  border: 1px solid #ccc;
  text-align: center;
}

/* Media query for mobile devices */
@media (max-width: 768px) {
  .container {
    grid-template-columns: repeat(2, 1fr); /* Two equal columns for mobile devices */
  }
}
`

3) Express - Create a server.js file with all of our standard express boilerplate. It should run at port 3001, send a message of "Server running" when it runs, and send a string of 'Welcome to our page' when reaching our landing page
`
// Importing required modules
const express = require('express');

// Creating an instance of Express
const app = express();

// Define a port for the server to listen on
const PORT = 3001;

// Middleware to log a message when server starts
app.listen(PORT, () => {
  console.log(`Server running on port ${PORT}`);
});

// Middleware to send 'Welcome to our page' on the landing page
app.get('/', (req, res) => {
  res.send('Welcome to our page');
});

// Middleware to handle 404 errors
app.use((req, res) => {
  res.status(404).send('404 - Not Found');
});
Explanation:
Express Setup: The express module is imported, and an instance of Express is created using const app = express();.
Server Listening: app.listen(PORT, () => { ... }) starts the server on port 3001 (PORT), and logs a message to the console when the server starts running.
Route Definition: app.get('/', (req, res) => { ... }) defines a route for the landing page ('/'). When a GET request is made to this route, it sends the response 'Welcome to our page'.
404 Handling: app.use((req, res) => { ... }) sets up a middleware to handle any requests that do not match a defined route. It responds with a 404 status code and the message '404 - Not Found'.
Usage:
Save the above code into a file named server.js.

Make sure you have Node.js installed on your system.

Open a terminal or command prompt, navigate to the directory containing server.js, and run the following command to install Express (if you haven't already):

'''npm install express'''

Once Express is installed, start the server by running: 

'''node server.js'''

You should see the message Server running on port 3001 in the terminal.

Open your web browser and navigate to http://localhost:3001/. You should see the message Welcome to our page.

This setup provides a basic Express server that listens on port 3001, sends a welcome message on the landing page, and handles 404 errors gracefully.




`
4) Django - Create a serializer that works off of two models, an author (parent) and a book (child) related by a PK and FK. Author has data of Name, Birth Date, Nationality, and if they are alive or not. Books have Title, Genre, and a Short Description of them

5) React - Use ChatGPT to tell you the differences between the UseContext hook and the Redux library, and the strengths, weaknesses, and usage for each would be. Then, using the information provided to you, teach it to your classmates

6) React - have ChatGPT explain what the "useState" hook is doing here:

```jsx

import { useState, useEffect } from 'react'
import axios from 'axios'

const App = () => {
    const [pokemon, setPokemon] = useState({})

    useEffect(()=> {
      const response = axios.get('https://pokeapi.co/api/v2/pokemon/squirtle')
      setPokemon(response.data)
      }, [])

    return (
     <div>
        <h1> {pokemon.name} </h1>
        <img src={pokemon.sprites.front_default} alt="sprite"/>
      </div

 )
}

export default App
```
