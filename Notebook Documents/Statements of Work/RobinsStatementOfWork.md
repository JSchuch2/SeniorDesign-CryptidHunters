# Statement of Work
## Andey Robins

Throughout this semester I've been a part of two of the central systems of our game: singly building and designing one and creating the lower framework for the other. Starting from the beginning, I conceptualized the way we would implement each piece of the AI and began the work on the low-level network physics handler. From there, it was a lot of reading as I learned about what the systems we would be trying to scale down and emulate do. For doing the key exchange and storing of weights and biases, I developed a way that leveraged Unity's built in filesystem to be able to perform all of the loading processes before the game even starts. I then wrote a simplified state machine where each state would be coupled to a specific kind of behavior that the AI could do. I took that system, and connected the state machine with a hard coded neural network that would calculate the appropriate time for the state machine to actually transition. From there, I developed a "sensor" based system that allowed us to create AI objects that interact with the gameworld. Whenever they trigger defined events, the continue into a new state machine by re-simulating the last segments and decisions of gameplay to avoid getting into the situation they ended up trapped in originially. Finally, I optimized and made it performant enough to operate during normal gameplay with only a mminimal impact on performance overall.