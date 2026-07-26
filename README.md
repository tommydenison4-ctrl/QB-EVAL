# QB Install Platform 1.0

A Vercel-ready React/Vite application for quarterback install training, audio transcription, AI evaluation, and staff reporting.

## Deploy to Vercel

1. Unzip this project.
2. Upload every file and folder to the root of a GitHub repository.
3. In Vercel, choose **Add New → Project** and import that repository.
4. Framework Preset should detect **Vite**. Do not add a custom Root Directory unless these files are in a subfolder.
5. Under **Environment Variables**, add:
   - `OPENAI_API_KEY` = your OpenAI API key
   - Optional: `OPENAI_GRADING_MODEL` = `gpt-5-mini`
6. Click **Deploy**.

There is no `functions` block in `vercel.json`; Vercel automatically detects the files in `/api`. This avoids the unmatched-function-pattern error from the prototype.

## Local development

```bash
npm install
npm run dev
```

The front end works locally, but transcription and AI grading require the Vercel functions or another compatible serverless environment with `OPENAI_API_KEY` configured.

## Current capabilities

- Game-day presentation: only the play call appears before the rep
- Browser audio recording
- Server-side OpenAI transcription
- Editable transcript
- AI grading by formation/alignment, routes/assignments, protection/scheme, reads/decisions, and situation
- Full install sheet revealed only after grading
- Local install manager with JSON import/export
- Staff dashboard with category gaps, play-level drill-down, transcripts, and progress chart
- York–McMaster 13-play test install included

## Important prototype limitation

Results are stored in the browser on the device being used. Supabase is not required for this version. Add cloud authentication, shared results, audio storage, and team-wide access later when the pilot workflow is proven.
