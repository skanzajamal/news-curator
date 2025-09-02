## Step 1: Create a New Project in Google Cloud Console

Go to the [Google Cloud Console](https://console.cloud.google.com/).

- Create a new project named **newsTLDR**.
- Click on the **Activate Cloud Shell** button on the top right and authorize access.

## Step 2: Initialize Node.js App

Once Cloud Shell is active, create a new directory and initialize a Node.js application:

```bash
mkdir news-curator
cd news-curator
npm init -y
```

## Step 3: Open the Editor

Click on the **Open Editor** button to edit in an IDE-like environment.

## Step 4: Create Basic Express API

Create an `index.js` file and paste the following code:

```javascript
import express from "express";
const app = express();
const PORT = process.env.PORT || 8080;

app.get("/", (req, res) => {
  res.send("Hello World");
});

app.listen(PORT, () => {
  console.log(`Server running on port ${PORT}`);
});
```

## Step 5: Configure Environment Variables

Create a `.env` file with the following variable:

```env
PORT=8080
```

## Step 6: Update `package.json`

Update your `package.json` to include the following:

```json
{
  "type": "module",
  "scripts": {
    "start": "node index.js",
    "dev": "nodemon index.js"
  }
}
```

## Step 7: Install Dependencies

Run the following command:

```bash
npm install express dotenv nodemon
```

## Step 8: Run the Application

Start your app with:

```bash
npm run dev
```

Your application will now run on port `8080`. Preview it in the browser by clicking the **Web Preview** button.

## Final Result

You should now see **Hello World** in your browser. 🎉

