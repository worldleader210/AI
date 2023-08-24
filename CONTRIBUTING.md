# Contributing
This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repositories using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
/*
Sylvina AI Chatbot

This program provides a function to simulate a chatbot named Sylvina.
Sylvina can respond to user inputs with predefined messages.

*/

// Setting up logging to monitor performance and errors
var logger:Logger = new Logger();
logger.setLevel(LoggerLevel.INFO);

function sylvinaAIChatbot(userInput:String):String {
    /*
        Sylvina AI Chatbot

            This function simulates a chatbot named Sylvina.
                It takes user input and returns a predefined response.

                    Parameters:
                        userInput (String): The user's input.

                            Returns:
                                String: The chatbot's response.

                                    Examples:
                                        trace(sylvinaAIChatbot("Hello"));
                                            // Output: "Hello! How can I assist you today?"

                                                trace(sylvinaAIChatbot("What's the weather like?"));
                                                    // Output: "I'm sorry, I am not programmed to provide weather information."

                                                        */
                                                            try {
                                                                    logger.info("Processing user input...");
                                                                            
                                                                                    // Convert user input to lowercase for case-insensitive matching
                                                                                            var input:String = userInput.toLowerCase();
                                                                                                    
                                                                                                            // Predefined responses
                                                                                                                    if (input.indexOf("hello") != -1 || input.indexOf("hi") != -1) {
                                                                                                                                return "Hello! How can I assist you today?";
                                                                                                                                        } else if (input.indexOf("goodbye") != -1 || input.indexOf("bye") != -1) {
                                                                                                                                                    return "Goodbye! Have a great day!";
                                                                                                                                                            } else {
                                                                                                                                                                        return "I'm sorry, I am not programmed to respond to that.";
                                                                                                                                                                                }
                                                                                                                                                                                    } catch (error:Error) {
                                                                                                                                                                                            logger.error("An error occurred: " + error.message);
                                                                                                                                                                                                    return "Oops! Something went wrong. Please try again later.";
                                                                                                                                                                                                        }
                                                                                                                                                                                                        }

                                                                                                                                                                                                        // Example usage
                                                                                                                                                                                                        trace(sylvinaAIChatbot("Hello"));