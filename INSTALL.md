## Create a basic Express API

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).

- Create a new project named **newsTLDR**.
- Click on the **Activate Cloud Shell** button on the top right and authorize access.


2. Once Cloud Shell is active, create a new directory  called news-curator and initialize a Node.js app by running following commands::

```bash
mkdir news-curator
cd news-curator
npm init -y
```

3. Once done, Click on the **Open Editor** button to edit in an IDE.

4. Let's set up a basic Express API endpoint by pasting in the following code in index.js:

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

5. Create a `.env` file with the following variable:

```env
PORT=8080
```

6. Next, update package.json by adding following scripts and also updating the type to module to support import statements.

```json
{
  "type": "module",
  "scripts": {
    "start": "node index.js",
    "dev": "nodemon index.js"
  }
}
```

7. Let's Open Terminal and install the packages we need:

```bash
npm install express dotenv nodemon
```

8. Start your app with:

```bash
npm run dev
```

Your application will now run on port `8080`. Preview it in the browser by clicking the **Web Preview** button.


You should now see **Hello World** in your browser. 🎉

