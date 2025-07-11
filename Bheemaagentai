import os
from langchain_together import ChatTogether

# Set API key
os.environ["TOGETHER_API_KEY"] = "tgp_v1_BvPlhwF-WQfAOBUmnV8OLm37Sdzbqmp9Uu8faPNSeIA"

# Initialize LLM with Together AI endpoint
llm = ChatTogether(
    model="mistralai/Mixtral-8x7B-Instruct-v0.1",
    temperature=0,
    max_tokens=512,
)

def main():
    print("Welcome to the AI Chatbot!")
    while True:
        query = input("You: ")
        if query.lower() == "exit":
            print("Goodbye!")
            break
        try:
            response = llm.invoke(query)
            if response:
                print("AI:", response)
            else:
                print("AI: No response generated.")
        except Exception as e:
            print("Error:", str(e))

if __name__ == "__main__":
    main()
