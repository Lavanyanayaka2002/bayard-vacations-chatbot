import streamlit as st

st.set_page_config(page_title="Bayard Vacations Chatbot")

st.title("🌍 Bayard Vacations AI Chatbot")
st.write("Ask me about travel packages, destinations, pricing, or booking process.")

def chatbot_response(user_input):
    user_input = user_input.lower()

    if "package" in user_input:
        return "We offer domestic and international holiday packages including honeymoon, family, and group tours."

    elif "destination" in user_input:
        return "Popular destinations include Goa, Kerala, Bali, Maldives, Dubai, and Europe."

    elif "price" in user_input or "cost" in user_input:
        return "Our packages start from ₹15,000 per person. Prices vary based on destination and duration."

    elif "booking" in user_input or "process" in user_input:
        return "You can book by contacting our travel expert, selecting a package, confirming details, and making payment."

    elif "contact" in user_input:
        return "You can reach Bayard Vacations via phone or email for personalized assistance."

    else:
        return "I'm here to help with travel packages, destinations, pricing, and booking details."

user_input = st.text_input("You:")

if user_input:
    response = chatbot_response(user_input)
    st.text_area("Chatbot:", response, height=100)
