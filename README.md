# Music Player Application

This is a Java application for managing playlists and songs within a music player. It allows users to create, manage, and share playlists, as well as interact with songs by liking, disliking, and listening to them.

## Features

- **Playlist Management**: Users can create, delete, and customize playlists.
- **Song Interaction**: Users can like, dislike, and listen to songs.
- **User Library**: Each user has a library containing their playlists.
- **Sharing**: Users can share playlists with other users.

## Classes

### 1. User
- Represents a user in the music player application.
- Attributes:
  - `username`: The username of the user.
  - `library`: A list containing all the playlists the user has created or added.
  - `currentlyPlaying`: The song the user is currently listening to.
- Methods:
  - `createPlaylist(String title, int age)`: Creates a new playlist.
  - `addPlaylist(Playlist playlist)`: Adds a playlist to the user's library.
  - `removePlaylist(String title)`: Removes a playlist from the user's library.
  - `likeSong(Song song)`: Likes a song and adds it to the "Liked" playlist.
  - `dislikeSong(Song song)`: Dislikes a song.
  - `likePlaylist(Playlist playlist)`: Likes a playlist.
  - `dislikePlaylist(Playlist playlist)`: Dislikes a playlist.
  - `sharePlaylist(User user, int index)`: Shares a playlist with another user.
  - `playSong(Song song)`: Sets the currently playing song.
  - `pauseSong(Song song)`: Pauses the currently playing song.
  - `toString()`: Returns a string representation of the user.

### 2. Playlist
- Represents a playlist in the music player application.
- Attributes:
  - `title`: The title of the playlist.
  - `owner`: The user who created the playlist.
  - `dateCreated`: The date the playlist was created.
  - `songs`: A list containing the songs in the playlist.
  - `duration`: The total duration of the playlist.
  - `likes`: The number of likes for the playlist.
  - `dislikes`: The number of dislikes for the playlist.
- Methods:
  - `addSong(Song song)`: Adds a song to the playlist.
  - `removeSong(Song song)`: Removes a song from the playlist.
  - `toArray()`: Converts songs to an array.
  - `topAndWorstSong()`: Returns the top and worst songs in the playlist.
  - `toString()`: Returns a string representation of the playlist.
  - `compareTo(Playlist other)`: Compares playlists based on creation date.

### 3. Song
- Represents a song in the music player application.
- Attributes:
  - `title`: The title of the song.
  - `duration`: The duration of the song in minutes.
  - `likes`: The number of likes for the song.
  - `dislikes`: The number of dislikes for the song.
- Methods:
  - `compareTo(Song other)`: Compares songs based on like factor.
  - `equals(Object obj)`: Checks if two songs are equal.
  - `toString()`: Returns a string representation of the song.

## Usage

To use the application, follow these steps:

1. Create instances of `User`, `Playlist`, and `Song` as needed.
2. Use methods provided by each class to manage playlists, songs, and user interactions.
3. Test the application to ensure proper functionality.
