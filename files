import random

print("Simple Chatbot")
print("==============")
print("Type 'bye' or 'quit' to exit\n")

conversation_history = []

greetings = ["hello", "hi", "hey", "greetings", "sup", "what's up"]
greeting_responses = [
    "Hi there! How can I help you today?",
    "Hello! What can I do for you?",
    "Hey! Nice to chat with you!",
    "Hi! How are you doing?"
]

farewell = ["bye", "goodbye", "quit", "exit", "see you"]
farewell_responses = [
    "Goodbye! Have a great day!",
    "See you later!",
    "Bye! Take care!",
    "Thanks for chatting! Goodbye!"
]

how_are_you = ["how are you", "how do you do", "how's it going", "what's up"]
how_are_you_responses = [
    "I'm doing great, thanks for asking! How about you?",
    "I'm fine, thank you! How are you?",
    "All good here! What about you?",
    "Doing well! How can I help you today?"
]

name_questions = ["what's your name", "who are you", "your name"]
name_responses = [
    "I'm a simple chatbot built with Python!",
    "You can call me ChatBot! I'm here to help!",
    "I'm your friendly Python chatbot!"
]

joke_keywords = ["joke", "funny", "laugh"]
jokes = [
    "Why don't programmers like nature? It has too many bugs! 😄",
    "Why do Python programmers prefer dark mode? Because light attracts bugs! 😂",
    "What's a programmer's favorite hangout? The Foo Bar! 🍺"
]

help_keywords = ["help", "what can you do", "capabilities", "commands"]
help_responses = [
    "I can chat with you, answer simple questions, and keep you company!",
    "I can respond to greetings, tell jokes, and have conversations with you!",
    "Try asking me about my name, how I'm doing, or ask me to tell a joke!"
]

thanks_keywords = ["thank", "thanks", "appreciate"]
thanks_responses = [
    "You're welcome!",
    "Happy to help!",
    "No problem at all!",
    "Anytime!"
]

def get_response(user_input):
    user_input = user_input.lower().strip()
    
    if any(word in user_input for word in farewell):
        return random.choice(farewell_responses), True
    
    if any(word in user_input for word in greetings):
        return random.choice(greeting_responses), False
    
    if any(phrase in user_input for phrase in how_are_you):
        return random.choice(how_are_you_responses), False
    
    if any(phrase in user_input for phrase in name_questions):
        return random.choice(name_responses), False
    
    if any(word in user_input for word in joke_keywords):
        return random.choice(jokes), False
    
    if any(word in user_input for word in help_keywords):
        return random.choice(help_responses), False
    
    if any(word in user_input for word in thanks_keywords):
        return random.choice(thanks_responses), False
    
    default_responses = [
        "That's interesting! Tell me more.",
        "I see. What else would you like to talk about?",
        "Hmm, I'm not sure about that. Can you rephrase?",
        "Interesting point! What do you think about it?",
        "I'm still learning! Try asking me something else."
    ]
    return random.choice(default_responses), False

while True:
    user_input = input("You: ")
    
    if not user_input.strip():
        continue
    
    conversation_history.append(f"You: {user_input}")
    
    response, should_exit = get_response(user_input)
    print(f"Bot: {response}\n")
    
    conversation_history.append(f"Bot: {response}")
    
    if should_exit:
        break

print(f"Conversation ended. Total messages: {len(conversation_history)}")