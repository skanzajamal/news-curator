# tldr
"Too Long; Didn't Read" (TL;DR) tech news application. 

This project leverages the Gemini API with Google Search grounding to deliver personalized news curation.

The application is deployed on Cloud Run, where it serves as a backend service.

🚀 Features

Personalized News Curation – Generates tailored news summaries using the Gemini API.

Google Search Grounding – Enhances responses with up-to-date, reliable information.

Cloud-Native Deployment – Runs on Cloud Run for scalability and cost efficiency.

🏗️ Architecture

User request triggers the Cloud Run service.

Cloud Run app queries the Gemini API with Google Search grounding.

Curated news response is generated.




