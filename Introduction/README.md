# Introduction & Setup

Node.js is a powerful and popular runtime environment that allows developers to build fast, scalable, and efficient server-side applications using JavaScript. It is built on the V8 JavaScript engine, which is also used by Google Chrome, and provides a rich set of tools and modules for developing web applications, network servers, and command-line tools.

To set up Node.js, you first need to download and install it on your machine. You can download the latest version of Node.js from the official website (https://nodejs.org). Once downloaded, simply run the installation file and follow the on-screen instructions to install Node.js on your machine.

After installation, you can verify that Node.js is working correctly by opening a terminal or command prompt and typing `node -v`. This should output the version of Node.js that you have installed.

To start building applications with Node.js, you will also need a code editor or IDE, such as Visual Studio Code, Atom, or Sublime Text. Once you have your editor set up, you can create a new project directory and start writing your first Node.js application.

Overall, Node.js is a powerful tool for building scalable, efficient, and modern web applications. With its vast ecosystem of modules and tools, it provides developers with everything they need to build robust server-side applications using JavaScript.

# Your first Node.js application

Let's start by creating a simple Node.js application that outputs a message to the console. To do this, open your code editor and create a new file called `app.js`. In this file, add the following code:

```js
console.log("Hello World!");
```

Now, open a terminal or command prompt and navigate to the directory where you saved the `app.js` file. Once there, type `node app.js` to run the application. You should see the following output:

```bash
Hello World!
```

Congratulations! You have just created and run your first Node.js application.

You can find the source code for this application in the `introduction\yourFirstApp` directory.

# The REPL

Node.js comes with a built-in REPL (Read-Eval-Print-Loop) environment that allows you to execute JavaScript code directly from the terminal. To start the REPL, simply open a terminal or command prompt and type `node`. You should see the following output:

```bash
> _
```

The REPL is a great tool for experimenting with Node.js and JavaScript. You can use it to test out new features, debug your code, and even build small applications.

To exit the REPL, simply type `.exit` and press the `Enter` key.

# The Global Object

The global object is a special object that is available in all Node.js applications. It represents the global scope of an application and provides a number of useful features, such as the ability to access the command-line arguments, the current working directory, and the operating system platform.

To access the global object, simply type `global` in the REPL. You should see the following output:

```bash
> global
{ ArrayBuffer: [Function: ArrayBuffer],
  Int8Array: { [Function: Int8Array] BYTES_PER_ELEMENT: 1 },
  Uint8Array: { [Function: Uint8Array] BYTES_PER_ELEMENT: 1 },
  ...
  }
```

The global object is also available in all JavaScript files. You can access it by simply typing `global` in your code.

```js
console.log(global);
```

# Process Object

The process object is a global object that provides information about, and control over, the current Node.js process. It can be accessed using the `process` global variable. The process object provides a number of useful properties and methods that allow you to interact with the current process in different ways.

For example, the `process.argv` property returns an array containing the command-line arguments passed when the Node.js process was launched. The first element will be `node`, the second element will be the name of the JavaScript file. The next elements will be any additional command-line arguments.

```js
console.log(process.argv);
```

While running the above code, you can pass additional command-line arguments to the process. For example, if you run the code using the following command:

```bash
node process.js one two=three four
```

You should see the following output:

```bash
[ 'node', 'process.js', 'one', 'two=three', 'four' ]
```

The `process.cwd()` method returns the current working directory of the Node.js process.

```js
console.log(`Current directory: ${process.cwd()}`);
```

The `process.platform` property returns a string identifying the operating system platform on which the Node.js process is running.

```js
console.log(`Current platform: ${process.platform}`);
```
