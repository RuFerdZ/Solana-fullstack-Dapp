<h1>Introduction to Solana</h1>

<img src="https://dev-to-uploads.s3.amazonaws.com/uploads/articles/nl0h25rp5h9ytg5wnrj7.png">

<h2>Project Overview</h3>


<ul>
    <li><a href="https://nodejs.org/en/" target="_blank">Node.js</a></li>
    <li><a href="https://docs.solana.com/cli/install-solana-cli-tools" target="_blank">Solana Tool Suite</a></li>
    <li><a href="https://project-serum.github.io/anchor/getting-started/introduction.html" target="_blank">Anchor framewoek</a></li>
    <li><a href="https://phantom.app/" target="_blank">Phantom solana wallet</a></li>
    <li><a href="https://reactjs.org/" target="_blank">React</a></li>
</ul>

<h2>Project Structure</h2>
In this project, you'll see four main folders (in addition to the node_modules):

<ul>
    <li><b>app</b> - Where our frontend code will go</li>
    <li><b>programs</b> - This is where the Rust code lives for the Solana program</li>
    <li><b>test</b> - Where the JavaScript tests for the program live</li>
    <li><b>migrations</b> - A basic deploy script</li>
</ul>


<h2>To build</h2>

1. Clone the repo

```sh
git clone git@github.com:dabit3/complete-guide-to-full-stack-solana.git
```

2. Change into the project directory you'd like to run

3. Install the dependencies

```sh
npm install
```

4. Start a local Solana node

```sh
solana-test-validator
```

5. Build the anchor project

```sh
anchor build
```

6. Fetch the project ID for the build:

```sh
solana address -k target/deploy/<programname>-keypair.json
```

6. Update the project ID in the Rust program located at __projectname/programs/src/programname.rs__ with the output from above.

7. Run the tests

```sh
anchor test
```

8. Change into the __app__ directory and install the dependencies:

```sh
cd app && npm install
``` 

9. Run the client-side app

```sh
npm start
```