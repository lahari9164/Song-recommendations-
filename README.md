~Song Recommendation System A simple Python-based project that recommends songs to the user based on their mood and preferred genre. Built using Google Colab, Python, and a CSV dataset.

~Features
Reads song data from a CSV file Filters songs by: Mood (happy, sad, chill, romantic, energetic, confident) Genre (pop, rock, indie, lofi, etc.) Case-insensitive search Displays matching song recommendations Easy to customize or expand with more data

~ Technologies Used P
ython Pandas Google Colab CSV dataset (songs.csv)

~Project Structure 
songs.csv song_recommendation_system.ipynb

~How It Works 
The program loads songs.csv using pandas. It converts the mood and genre values to lowercase for consistency. The user inputs: Their mood Their preferred genre The program filters the CSV and displays all songs that match both. If no matches are found, it prints a helpful message.

~Code Snippet (Core Logic) 
import pandas as pd df = pd.read_csv("songs.csv") df["mood"] = df["mood"].str.lower() df["genre"] = df["genre"].str.lower() print("\nSONG RECOMMENDATION SYSTEM READY ✔\n") user_mood = input("Enter your mood (happy / sad / chill / romantic / energetic / confident): ").strip().lower() user_genre = input("Enter preferred genre: ").strip().lower() filtered = df[(df["mood"] == user_mood) & (df["genre"] == user_genre)] if filtered.empty: print("\nNo songs found for this mood + genre combination.") else: print("\nRecommended Songs:\n") for i, row in filtered.iterrows(): print(f"- {row['song']} by {row['artist']}")

~Sample songs.csv Format song,artist,mood,genre See You Again,Tyler the Creator,Hip-Hop,romantic The Less I Know The Better,Tame Impala,Psych Rock,romantic Do I Wanna Know?,Arctic Monkeys,Rock,sad Daddy Issues,The Neighbourhood,Indie,sad Woman,Doja Cat,Pop,confident My Kind of Woman,Mac DeMarco,Indie,romantic

~Future Improvements
Add multi-genre recommendation Add recommendation based on BPM or popularity GUI version using Tkinter or Streamlit Add audio preview links

~Contributions Feel free to fork this project and enhance the dataset or add new features
