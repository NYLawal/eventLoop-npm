QUESTION 1
The Event Loop is a fundamental part of Node.js that allows it to perform non-blocking I/O operations by offloading operations to the system kernel whenever possible. Since Node.js is single-threaded, the event loop is what enables asynchronous programming by ensuring that the main thread is not blocked. The role of this loop is to schedule which operations the single thread should be performing at any given point in time.


QUESTION 2
The six phases of the event loop are: timers, pending callbacks, idle-prepare, poll, check and close callbacks.

Timers: It is the first phase in the event loop which executes callbacks scheduled by setTimeout() and setInterval(). It finds expired timers in every iteration (also known as Tick) and executes the timers callbacks.

Pending callbacks: This executes I/O callbacks deferred to the next loop iteration. This is where any special system events are run. For example, a TCP socket throwing a connection refused error.

Idle-prepare: This phase is only used internally.

Poll: In this phase, I/O related callbacks are executed. Additionally, the polling phase waits for more input/output callbacks, calculates how long it should wait before going on to the next phase, and if the queue is empty, it moves on to the fifth phase. All callbacks are synchronously called in the order in which they were added to the queue, from oldest to newest. 

Check: This phase handles the callbacks scheduled by setImmediate(), and the callbacks will be executed once the Poll phase becomes idle.

Close callbacks: This phase executes the callbacks of all close events. This is the point at which the Event Loop has completed one cycle and is ready to go on to the next. If there are no timers or input/output calls left, the event loop closes and the process ends. It is primarily used to clear the application's state.


QUESTION 3 // Best practices in server-side code development
1. Focus on code quality i.e use tools for creating consistency and reducing developer errors when writing code e.g Prettier formatter and ESLint.
2. Make code more maintainable and readable. For example, using the ES6 standard of JavaScript and using promises or Async/Await to handle asynchronous calls.
3. Keep code small by taking advantage of modules. In building an application, one might want to consider employing microservices architecture rather than monolith architecture since it encourages modularisation.
4. Handle errors by making both the user and the developer aware of possible errors in the code. The user should be presented with feedback about what has happened and a solution to continue using the application while the developer should be presented with relevant error messages to locate and correct errors.


QUESTION 4
NPM is a JavaScript package manager. It is a website hosting more than 1 million third-party packages that can be used for our project, it is also a command line tool used for managing project dependencies. 


QUESTION 5
To initialise a package in NPM, the 'npm init' command is used if we want to go through all of the settings. Otherwise, we use 'npm init -y' to select all defaults. Either of this will create a package where the project files will be stored.


QUESTION 6
To run a script in the package.json, we use the 'npm run name-of-script' command, where name-of-script is the name of the script that we have added to our package.json file. For example: npm run prettier




