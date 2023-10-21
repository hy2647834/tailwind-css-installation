# tailwindcss Installation

## Step - 1:

- npm init -y (This will create package.json file)

## Step - 2:

- create folder with name 'public'
- we will store index.html and css file here.

## Step - 3:

- Goto tailwind css documentation [ https://tailwindcss.com/docs/installation ]

- Install **tail wind css** dependency via cli using the following command

  ```
  npm install -D tailwindcss
  (This will update tailwind css as dev dependency in package.json)
  ```

- Run the following command to create **tailwind css config js** file

  ```
  npx tailwindcss init
  ```

## Step - 4:

- Configuring the templates path

  - Add the following in **tailwind.config.js** file

    ```
    content: ["./public/*.{html}"],
    ```

## Step - 5:

- Create a folder **src**, then create new file **input.css**

  - Add the below lines in **input.css** file

    ```
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    ```

## Step - 6:

- Command to generate **style.css** as output file with **watch** flag

  ```
  npx tailwindcss -i ./src/input.css -o ./public/style.css --watch
  ```

## Step - 7:

- Configuring the **build** script of tail wind css file in **package.json**

  Add below line in package.json

  ```
  "build": "tailwindcss -i ./src/input.css -o ./public/style.css --watch"
  ```

  Use the below command to run the above script

  ```
  npm run build
  ```

## Step - 8:

- Linking **index.html** file with generated **style.css** file.

  ```
  <link rel="stylesheet" href="style.css">
  ```

### Video credits

- https://www.youtube.com/watch?v=SPr-1cwVn1k&list=PLKKoWAz_o0UjvmIT7f61HF5HMM1F9G1kS
