RAKINA TRANSFER NEWS - LIVE FEED PACKAGE

IMPORTANT:
- This package is designed for a Netlify site deployed from a connected Git repository/build, so Netlify can deploy the serverless function.
- A simple drag-and-drop static deploy may not deploy the function.
- The function reads the secret API key from an environment variable called API_FOOTBALL_KEY.
- Do NOT put your API key in index.html or share it publicly.

SETUP:
1. Upload these files to a GitHub repository (index.html, netlify.toml, and netlify/functions/transfers.js).
2. In Netlify, import/connect that GitHub repository and deploy it.
3. In Netlify site settings, go to Environment variables and add:
   Key: API_FOOTBALL_KEY
   Value: your private API-Football key
   Scope: Functions (or all scopes if Functions-only is not offered)
4. Redeploy the site after saving the variable.
5. Open the site and press "Load transfer updates".

LIMITATIONS:
- API-Football's /transfers endpoint requires a player or team ID. This starter function queries a curated list of 12 major clubs to stay mindful of the free daily request limit.
- Results are transfer records for those clubs, not a comprehensive real-time worldwide news/rumour feed. It may include historical records. It does not automatically fetch every club in the world.
- The API provider's terms and available data coverage apply. Check API-Football pricing/docs before publishing at scale.
- Replace the contact placeholder and complete privacy information before applying for ads.
