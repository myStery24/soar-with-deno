# Soar with Deno

StackUp <> Deno Campaign

## Prerequisites

Before running the project, ensure you have the following installed:

- [Deno](https://deno.land/) - A secure runtime for JavaScript and TypeScript.

## Usage

### Generate an API Key

To generate your API key, run the following command:

```bash
deno run generateToken.ts
```

### Replace API Key

1. Open the `.env.example` file.  
2. Copy the generated API key (output from the previous command) and replace `YOUR_API_KEY` in the file:  

   ```plaintext
   API_KEY="YOUR_API_KEY"
   ```

3. Rename the file from `.env.example` to `.env`.  

Your `.env` file is now configured and ready for use!

## Running the Project

To start the application, use the following command:

```bash
deno run --allow-env --allow-net main.ts
```

### Permissions Explained:
- `--allow-env`: Grants access to environment variables.
- `--allow-net`: Grants access to the network for the server to run.

## Project Structure

```
.
├── crypto/
│   ├── auth.ts          # Handles authentication logic
│   ├── jwt.ts           # JWT utilities for token handling
│   └── pwd.ts           # Password hashing and verification
├── database/
│   ├── mod.ts           # Database initialization and helpers
│   └── users.db         # SQLite database file
├── middleware/
│   ├── login.ts        
│   ├── mod.ts          
│   ├── register.ts            
│   └── auth/            # Middleware for authentication routes
│       ├── deleteAccount.ts
│       └── updateAccount.ts
├── types/               # TypeScript types and interfaces
│   ├── request.ts
│   └── user.ts
├── .env.example         # Environment variables template
├── .gitignore         
├── cookie.cookie
├── deno.json            # Configuration for dependencies
├── generateToken.ts     # Script to generate API keys
└── main.ts              # Entry point for the application
```