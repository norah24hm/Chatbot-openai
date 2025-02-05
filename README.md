## OpenAI chat completion 
The project idea is to build a chat interface with OpenAI chat completion  which is an AI technology that allows computers to understand and respond to human input in a conversational manner.
### Steps:
1. Get OpenAI API Key: You'll need to sign up for an OpenAI API key, which is required to access the OpenAI chat completion API. You can sign up for a free API key on the OpenAI website.
2. Setup : The programming language used in this project is python for that you need to start by setting up Python on your device by following these steps:
   
   * Install Python
   * Install the OpenAI Python library
   * Set up a virtual environment (optional)
   * Set up your API key 
   * Sending your API request
  
   All the detailes about gettin up and running with the OpenAI API for different operaing systems and different languages are provided here:  https://platform.openai.com/docs/quickstart

3. HTML and CSS: You'll need to create an HTML file to define the structure of your chat interface, and a CSS file to style it. You can use any text editor or IDE to create these files such as vs code.

4. JavaScript: You'll need to write JavaScript code to interact with the OpenAI API, process user input, and display the response.
5. Get http client: Such as Axios which is a JavaScript library, specifically a http client library. It's a popular, open-source library used for making http requests in JavaScript applications allowing us to fetch data, send data, and perform other http-related tasks.
  * To make API request using js we can use js code or using Axios cdn link that allow us to include the Axios library in your html file without installing it via npm or yarn, it is 
    available on : https://cdnjs.com/libraries/axios


### Demo:


https://github.com/user-attachments/assets/1208cc71-9d5f-4290-b79c-69335b2fb381


https://github.com/user-attachments/assets/aa5ae54c-8805-48b1-8196-0e867ecc6aa9

-------------------------------------------------------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------------------------------------------------------



## Python chatbot:

* We can write a simple python code using OpenAI API chat completion that takes the user's input and display a response generated by openai.
* After the installation and setting up as mentioned previously, we should create a folder that contains a .env file then initialize and declare a variable for the openai key.
* Then create a python file and use the code below:
  
  ```
  # Import the OpenAI library
  from openai import OpenAI
  
  ```

  ```
  # Create an instance of the OpenAI client
  client = OpenAI()
  ```
  ```
  # Define a function to send a message to the chatbot and get a response
  def send_message(message_log):
  ```
  ```
  # Create a chat completion request with the user's message
  completion = client.chat.completions.create(

  # Specify the model to use (in this case, gpt-4)
        model="gpt-4",
  # Define the message to send to the chatbot
        messages=[
        {"role": "user", "content": message_log}
        ]  
    )
  ```
  ```
  # Get the response from the chatbot
  # If no response with text is found, return the first response's content (which may be empty)
  return completion.choices[0].message.content
  ```

  ```
  # Define the main function that runs the chatbot
  def main():
   print("Welcome to the chatbot! Type 'quit' to exit.")
  ```

  ```
  # Run an infinite loop to keep the chatbot running
  while True:
        # Get the user's input
        user_input = input("You: ")
  ```
  ```

  # Check if the user wants to quit
        if user_input.lower() == "quit":
            print("Goodbye!")
            break
  ```
  

  ```
  # Send the user's input to the chatbot and get a response
        response = send_message(user_input)
        # Print the chatbot's response
        print(f"AI assistant: {response}")
  
  ```

  ```
  # Run the main function 
   if __name__ == "__main__":
    main()
  ```

  #### The output:
  ![python chatbot](https://github.com/user-attachments/assets/5ce5c586-e4ac-4954-8c61-2f9e67c621d0)
