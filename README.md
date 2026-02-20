# RAG App - Retrieval-Augmented Generation

A Next.js application with Retrieval-Augmented Generation (RAG) capabilities, database integration via Drizzle ORM, and AI-powered embeddings.

## Features

- **RAG System**: Retrieve and augment information for AI responses
- **AI Embeddings**: Generate and store document embeddings
- **Database**: PostgreSQL/Neon with Drizzle ORM migrations
- **Chat API**: RESTful endpoint for chat interactions
- **Styling**: Tailwind CSS with shadcn/ui components

## Tech Stack

- **Framework**: Next.js 14+
- **Language**: TypeScript
- **Database**: Neon PostgreSQL with Drizzle ORM
- **Styling**: Tailwind CSS
- **UI Components**: shadcn/ui
- **Environment**: Node.js 18+

## Project Structure

```
my-rag-app/
├── app/                    # Next.js app directory
│   ├── api/chat/          # Chat API endpoint
│   ├── layout.tsx         # Root layout
│   ├── page.tsx           # Home page
│   └── globals.css        # Global styles
├── components/            # React components
│   └── ui/               # shadcn/ui components
├── lib/                   # Utility functions
│   ├── actions/          # Server actions
│   ├── ai/               # AI utilities (embeddings)
│   └── db/               # Database config and migrations
├── public/               # Static assets
└── package.json          # Dependencies
```

## Installation

```bash
# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local
# Edit .env.local with your configuration

# Run database migrations
npm run db:migrate
```

## Environment Variables

Create a `.env.local` file:

```env
# Database
DATABASE_URL=your_neon_db_url

# AI/LLM
OPENAI_API_KEY=your_api_key
# Add other AI provider keys as needed
```

## Development

```bash
# Start development server
npm run dev

# Open http://localhost:3000 in your browser
```

## Database

### Migrations

Migrations are stored in `lib/db/migrations/`. To run migrations:

```bash
npm run db:migrate
```

### Schema

Database schema is defined in `lib/db/schema/`:
- `embeddings.ts` - Vector embeddings storage
- `resources.ts` - Resource/document storage

## API Routes

### Chat Endpoint

- **URL**: `/api/chat`
- **Method**: POST
- **Description**: Process chat messages with RAG

## Building

```bash
npm run build
npm run start
```

## Contributing

1. Create a feature branch
2. Make your changes
3. Push to your fork
4. Submit a pull request

## License

MIT

## Support

For issues and questions, please open an issue on GitHub.
