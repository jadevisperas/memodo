import streamlit as st

# 1. Page Configuration (The "Vibe" Setup)
st.set_page_config(page_title="MEDMODO", page_icon="🔬", layout="wide")

# 2. Sidebar Navigation
st.sidebar.title("MEDMODO")
st.sidebar.markdown("---")
page = st.sidebar.radio("Navigate to:", ["Home", "Biotech Lab", "Memos", "Accountability"])

# 3. Logic for switching pages
if page == "Home":
    st.title("Welcome to the Lab 🌿")
    st.write("MEDMODO is your gateway to Biotechnology, Molecular Bio, and Microbio.")

elif page == "Biotech Lab":
    st.title("Biotechnology Workspace")
    # This is where your Python tools go
    dna = st.text_input("Paste a DNA sequence to translate:")
    if dna:
        st.success(f"Sequence received! Processed: {dna.upper().replace('T', 'U')}")

elif page == "Memos":
    st.title("Community Memos")
    st.write("Share your study progress or ask questions.")
    # You can add a simple text area for posting here later

elif page == "Accountability":
    st.title("Study Tracker")
    st.checkbox("Completed Microbio Chapter 1")
    st.checkbox("Practiced Python for Bio")
