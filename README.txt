QB INSTALL TRAINER V5

WHAT CHANGED
- Replaced unreliable browser SpeechRecognition with MediaRecorder.
- Press the microphone once to record and again to stop.
- Audio playback and download are available after every rep.
- Automatic football-aware transcription is available through the included secure Vercel server function.
- The OpenAI API key stays on the server and is never placed in index.html.
- The quarterback can still type or correct the transcript before grading.

GITHUB PAGES
GitHub Pages can host index.html and record/play audio over HTTPS.
It cannot securely store an OpenAI API key or run api/transcribe.js. Automatic transcription will therefore require a separate server endpoint. Recording itself will still work.

RECOMMENDED: VERCEL
1. Upload this entire folder to a GitHub repository.
2. Import that repository into Vercel.
3. In Vercel Project Settings > Environment Variables, add OPENAI_API_KEY.
4. Deploy.
5. Open the Vercel HTTPS URL. The default endpoint /api/transcribe will work automatically.

SECURITY
Never paste an OpenAI API key into index.html or commit it to GitHub.

MICROPHONE TROUBLESHOOTING
- Use HTTPS or localhost.
- Allow microphone access in the browser address bar.
- Close other apps that may exclusively control the microphone.
- Press once to start and once to stop; do not double-click.
