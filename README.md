# MIST4610-Project1-Group8

## Team Name: 
61608 Group 8

## Team Members:
1. Peng, Kimberly @[KimmyPenguin](https://github.com/KimmyPenguin)
2. Sivakumar, Srujana @[sruj-siva](https://github.com/sruj-siva)
4. Asgari, Neema @[Neemajoon](https://github.com/Neemajoon)
5. Modi, Maleeka @[m-modi](https://github.com/m-modi)
6. Palacherla, Asha @[ashapalacherla](https://github.com/ashapalacherla)

## Problem Description:

We chose this scenario because Spotify is one of the most popular music streaming services, with millions of users worldwide. The data model will allow us to better understand how various entities like songs, albums, and artists are interconnected in the system, which is highly relevant to both businesses in the music industry and tech professionals developing similar systems. With real-world applications, the model could be extended to track metrics like streams, monthly listeners, or the popularity of songs. This could serve as the foundation for building recommendation algorithms, analyzing user engagement, or making data-driven business decisions, which is crucial for the development of platforms similar to Spotify.


## Data Model: 

This database schema represents a structured design for a music streaming platform similar to Spotify. At its core, the artist table stores information about musicians, including their first and last names, biography, gender, and monthly listeners. Each artist is associated with a discography, which tracks their body of work and is linked through the discography_discography_id foreign key. 

The album table captures details about albums, including the title, release date, and references to both the artist and their discography. Each album contains multiple songs, stored in the song table, which records song titles, durations, genres, release dates, and the number of streams. Songs are linked to albums through album_album_id.


To track collaborations, the artist_has_song table establishes a many-to-many relationship between artists and songs, allowing for multiple artists on a single track. Similarly, playlists are managed through the playlist table, which includes details like title, save count, and creation date. The playlist_has_song table connects songs to playlists, enabling users to add multiple tracks to a playlist. Additionally, the playlist_has_artist table associates playlists with artists, making it possible to create artist-centric playlists. Overall, this schema efficiently structures relationships between artists, albums, songs, and playlists, facilitating seamless querying and management of music data in a SQL-based streaming platform.


## ERM Diagram:

![Image 3-13-25 at 2 43 PM](https://github.com/user-attachments/assets/c6f304c5-1533-473a-b55e-c73fd149ae54)

## Data Dictionary: 

Data Dictionary: Album
![Image 3-13-25 at 2 45 PM](https://github.com/user-attachments/assets/3987cdef-b566-4d22-a196-764e12408701)

Data Dictionary: Song
![Image 3-13-25 at 2 46 PM](https://github.com/user-attachments/assets/6e400a94-36d5-4dc5-ab2f-75e9baa31752)

Data Dictionary: Playlist
![Image 3-13-25 at 2 47 PM](https://github.com/user-attachments/assets/a3eb7f67-8abf-484d-93ef-892da39a4dd9)

Data Dictionary: Discography
![Image 3-13-25 at 2 47 PM (1)](https://github.com/user-attachments/assets/b55f7923-02ef-4b19-8442-60b55d6ecd1c)

Data Dictionary: artist has song
![Image 3-13-25 at 2 48 PM](https://github.com/user-attachments/assets/bf6247a1-221a-4cac-acc2-3e6912c29393)

Data Dictionary: playlist has song
![Image 3-13-25 at 2 48 PM (1)](https://github.com/user-attachments/assets/0e82496f-d1a2-46a0-9319-f9c61ac4edc2)

Data Dictonary: playlist has artist
![Image 3-13-25 at 2 53 PM](https://github.com/user-attachments/assets/def45731-e768-45f4-a095-c3f93561b47c)

## Queries: 

#1 C: Find the top three songs in the pop genre

This information helps us determine which pop songs are currently the most streamed and can even compare them to past trends. We can also identify audience preferences and common elements among the top pop songs, providing valuable insights into what drives their popularity.

![Image 3-13-25 at 3 00 PM](https://github.com/user-attachments/assets/b6e227e4-0d9d-490f-8d49-b974a635a58e)


#2 C: Find artists that are in popular playlists & count how many they appear in

Knowing how many playlists an artist appears in, as well as which playlists have the most amount of likes and listens is a great way to separate artists that appeal to listeners outside a specific genre, and general songs that a wide variety of users like to listen to regardless of their normal taste in music. Being able to find outliers like these is helpful to see what artists are able to reach listeners outside of their usual bubble.

![Image 3-14-25 at 11 46 AM](https://github.com/user-attachments/assets/f22c489e-7340-4a1e-bddc-69c6a52ea49e)

#3 C: Total streams of each genre in descending order 

This is important for a manager to know so that we can see which songs are popular within the genre versus the songs that have made waves outside of the genre and have reached a wider population and has accumulated some merit from a greater  audience than what the genre normally sees.

![Image 3-14-25 at 11 44 AM](https://github.com/user-attachments/assets/4f847245-0425-4c2f-97f7-3acce4cb0048)

#4 C: Show all artists with the number of albums they released

This is important to managers because of how important general artist stats are. Knowing how many albums (and subsequently, songs) an artist has released is important because this helps to see how much music an artist has made by any given time, which helps when considering streams and monthly listens.

![Image 3-14-25 at 12 05 PM](https://github.com/user-attachments/assets/f10a2f2d-b85f-4538-bd4d-15c877e28288)


#5 C: Find out if song exists in artists discography

This is important to managers because so many songs have been released throughout time and knowing if a song stuck in a users head is by a specific singer they might know, or if someone recommended a song but the user forgot the artists name, this search input lets them know that whichever artist they searched in has a released song by that name.

![Image 3-14-25 at 11 44 AM (1)](https://github.com/user-attachments/assets/85226800-7379-4af6-809f-3a1cba9d961e)


#6 C: Shows how many albums released by an artist each year

 This is important for managers to know in order to benchmark yearly releases and streams to be able see how many albums have been released in descending order by year, allowing us to get a full understanding of how many songs and albums and pacing of album releases various artists have had compared to other artists.

![Image 3-14-25 at 3 03 PM](https://github.com/user-attachments/assets/7b688622-940a-4de7-8fdb-44e5eb50b058)


#7 S: List top artist in each genre 

This is important to managers because this allows them to see who is currently at the top of the music game. This can give insights on how well a manager’s own artists are doing, as well as the competition. This can also be used to scope out potential musicians to collaborate with that can help increase the manager’s own artists popularity.

![Image 3-14-25 at 12 06 PM](https://github.com/user-attachments/assets/887339f6-1c55-495a-939c-49cca86801bc)


#8 C: Find a Song that was played less/more than X number of times with that artist information

Allows us to filter through songs the general population really likes, or really dislikes. By filtering every song by the number of streams it has, we are able to gain insights on what the general population likes to listen to, what the most and least streamed songs are, see basic artist and album information
![Image 3-13-25 at 2 57 PM](https://github.com/user-attachments/assets/a2872a58-abc7-4217-9669-39efa71fd44c)


#9 S: Finding out the most streamed songs

With this query, we gain insights into the popularity of a specific artist or song, uncover the key elements that contribute to a song's success, and identify patterns in music consumption. Additionally, we can analyze how factors such as genre, release date, and duration influence a song’s performance.

![Image 3-13-25 at 2 55 PM](https://github.com/user-attachments/assets/6a9d01ab-f84f-46f9-8a21-4cdc7b7750fc)

#10 S: Report all songs in the ‘pop’ category that have been added to any playlist

This is important to managers because we can see (by genre specifically) that suits the most number of people’s music taste. This helps with choosing top songs of any given genre, as well as makes it easier to curate genre-based playlists and Spotify Wrapped profiles to users who tend to stick to one genre/heavily prefer one genre over others.

![Image 3-14-25 at 11 43 AM](https://github.com/user-attachments/assets/6757fd39-5973-48c3-a93e-aca03423718d)




## Database Information: 

![Image 3-14-25 at 3 09 PM](https://github.com/user-attachments/assets/71772edc-9ff5-493c-bd88-9a3501928f0d)
















