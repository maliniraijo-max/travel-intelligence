# Travel Intelligence

Editorial travel discovery and Instagram carousel workspace.

## Initial scope
- Starting research area: North Paravur, Kerala
- Discovery radius: 20 km
- First test destination: Cherai Beach
- Initial content format: Instagram carousels
- Publishing policy: explicit human approval required

## What is included
- Responsive Next.js dashboard shell
- Editorial visual system (ivory, charcoal, olive, terracotta)
- Research brief input (UI preview only)
- Research/content/approval navigation
- Cherai Beach starter workspace card
- Supabase client scaffold and initial SQL schema
- Environment-variable template

## What is not connected yet
The first milestone is the application foundation. Research execution, AI generation, Meta OAuth, Instagram publishing, scheduling, and real database persistence are not active yet. The dashboard currently captures a brief only in local interface state.

## Requirements
- Node.js 20+
- npm
- A Supabase project (later milestone)
- OpenAI API key (later milestone)
- Meta developer app and Instagram Creator account (publishing milestone)

## Run locally
```bash
npm install
cp .env.example .env.local
npm run dev
```
Open http://localhost:3000.

## Deploy
1. Create a GitHub repository named `travel-intelligence`.
2. Push this project to the repository's `main` branch.
3. Import the repository into Vercel.
4. Add environment variables only when the corresponding integrations are implemented.
5. Deploy.

## Safety design
- No automatic publishing.
- Approval state must be persisted server-side before publishing is implemented.
- Keep OpenAI, Supabase service-role, and Meta secrets server-side.
- Do not store access tokens in browser storage.

## Next milestone
Implement the destination research pipeline with web search, source records, geographic filtering, and report persistence. Use Cherai Beach as the first test report.
