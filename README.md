# Vue Dischi

##  Description

This project was made with **Vue CLI** and it's inspired by **Spotify**.<br>
The main focus while making this project was the usage of ```props``` and ```custom events```.<br>
Each ```SongCard``` component is shown using the ```FilterSelect``` component wich emits an event everytime it changes value and filters the shown songs with the selected genre.

## Features

- **API call** to get songs.
- **Loading screen** shown until all songs get fetched (It will always be shown for 2 seconds for **didactic purposes**).

## Screenshots:

![spot1](https://user-images.githubusercontent.com/85038274/151706227-214a7906-f5e5-4767-aee7-a689a63219b6.PNG)

![spot2](https://user-images.githubusercontent.com/85038274/151706226-ec76a172-e617-421a-8bef-3a393b7af20f.PNG)

![spot3](https://user-images.githubusercontent.com/85038274/151706224-5ff1fb64-8bfb-4bb8-a806-c326866c5b5d.PNG)

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
