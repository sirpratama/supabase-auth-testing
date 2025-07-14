# Supabase Authentication Testing

A React application for testing Supabase authentication features, including Google OAuth and other authentication methods.

## Tech Stack

- **React 18** - JavaScript library for building user interfaces
- **Vite** - Fast build tool and development server
- **Supabase** - Backend-as-a-Service for authentication and database
- **Supabase Auth UI** - Pre-built authentication components
- **TailwindCSS** - Utility-first CSS framework

## Features

- ✅ **Email/Password Authentication**
- ✅ **Google OAuth Integration** 
- ✅ **Magic Link Authentication**
- ✅ **Session Management**
- ✅ **Protected Routes**
- ✅ **Responsive UI with Supabase Auth UI components**

## Prerequisites

- Node.js (v16 or higher)
- A Supabase project with authentication enabled
- Google OAuth credentials configured in Supabase

## Setup Instructions

1. **Clone and install dependencies:**
   ```bash
   git clone <your-repo-url>
   cd supabase-auth-testing
   npm install
   ```

2. **Configure Supabase:**
   - Create a `.env.local` file in the root directory
   - Add your Supabase credentials:
     ```env
     VITE_SUPABASE_URL=your_supabase_project_url
     VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
     ```

3. **Configure Google OAuth in Supabase:**
   - Go to your Supabase Dashboard → Authentication → Providers
   - Enable Google provider
   - Add your Google OAuth credentials
   - Set up redirect URLs for your domain

4. **Run the development server:**
   ```bash
   npm run dev
   ```

## Project Structure

```
src/
├── App.jsx          # Main app component with auth logic
├── App.css          # Application styles
├── main.jsx         # React app entry point
└── ...
supabaseClient.js    # Supabase client configuration
```

## Authentication Flow

1. **Unauthenticated users** see the Supabase Auth UI component
2. **Users can sign in** via email/password, magic link, or Google OAuth
3. **Authenticated users** see a simple "Logged in!" message
4. **Session management** is handled automatically by Supabase

## Important Notes

- This project uses **React 18** for compatibility with Supabase Auth UI
- The Supabase Auth UI library is deprecated (as of Feb 2024) but still functional
- For production apps, consider migrating to custom auth forms or the new Supabase UI Library

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## Troubleshooting

If you encounter authentication issues:

1. **Check your Supabase URL and API key** in the environment variables
2. **Verify Google OAuth setup** in Supabase Dashboard
3. **Ensure redirect URLs** match your development/production domains
4. **Check browser console** for specific error messages

## Contributing

This is a testing project for learning Supabase authentication patterns. Feel free to experiment with additional auth providers or UI improvements.
