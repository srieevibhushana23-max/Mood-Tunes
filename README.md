# Mood-Tunes
A Mood tunes is an kind of game which is relaxing your mind as current of your mood. 
import random

# 🎵 Step 1: Create a mood dictionary with songs
mood_songs = {
    "happy": [
        "Happy – Pharrell Williams",
        "Best Day of My Life – American Authors",
        "On Top of the World – Imagine Dragons",
        "Good as Hell – Lizzo",
        "Uptown Funk – Bruno Mars"
    ],
    "sad": [
        "Someone Like You – Adele",
        "Let Her Go – Passenger",
        "Fix You – Coldplay",
        "Stay With Me – Sam Smith",
        "Say Something – A Great Big World"
    ],
    "energetic": [
        "Eye of the Tiger – Survivor",
        "Can't Stop – Red Hot Chili Peppers",
        "Believer – Imagine Dragons",
        "Thunderstruck – AC/DC",
        "Stronger – Kanye West"
    ],
    "relaxed": [
        "Perfect – Ed Sheeran",
        "Let It Be – The Beatles",
        "Sunflower – Post Malone",
        "Banana Pancakes – Jack Johnson",
        "Photograph – Ed Sheeran"
    ]
}

# 🎧 Step 2: Display mood options
print("🎶 Welcome to MoodTunes – Your Mood-Based Music Recommender 🎶")
print("\nAvailable moods:")
for mood in mood_songs.keys():
    print(f" - {mood.capitalize()}")

# 🎤 Step 3: Get user mood input
user_mood = input("\nEnter your mood: ").lower()

# 🎲 Step 4: Suggest a random song
if user_mood in mood_songs:
    song = random.choice(mood_songs[user_mood])
    print(f"\nBased on your mood ({user_mood.capitalize()}), we recommend: 🎧 {song}")
else:
    print("\nSorry, I don't recognize that mood yet! Try again with: happy, sad, energetic, or relaxed.")

# 🪄 Step 5 (Optional): Ask to continue
while True:
    again = input("\nWould you like another song suggestion? (yes/no): ").lower()
    if again == "yes":
        song = random.choice(mood_songs.get(user_mood, []))
        print(f"🎵 Try this one: {song}")
    else:
        print("\nThanks for using MoodTunes! 🎶 Have a great day! 💫")
