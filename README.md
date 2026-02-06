# Smart Alumni Connect

A comprehensive full-stack Alumni Engagement Platform built with React, TypeScript, and Supabase. This platform enables colleges and universities to maintain strong connections with their alumni through a centralized digital ecosystem.

## Features

### Core Functionality

1. **User Authentication & Profiles**
   - Secure email/password authentication
   - Role-based access control (Alumni, Students, Admins)
   - Comprehensive user profiles with education and career information
   - Mentorship availability settings

2. **Alumni Directory**
   - Browse and search alumni by name, company, major
   - Filter by role and mentorship availability
   - Connect with other alumni
   - View detailed profiles with career information

3. **Job Board**
   - Post and browse job opportunities
   - Filter by job type (full-time, part-time, internship, contract)
   - Detailed job descriptions with application links
   - Alumni can share career opportunities with the community

4. **Events Management**
   - Create and manage virtual and in-person events
   - RSVP functionality with attendee tracking
   - Support for various event types (meetups, webinars, reunions, workshops, fundraisers)
   - Event capacity management

5. **Donation Portal**
   - Support multiple fundraising campaigns
   - Anonymous donation options
   - Real-time progress tracking
   - Donor recognition wall

6. **Admin Dashboard**
   - Platform analytics and statistics
   - User management overview
   - Quick access to all platform features
   - System health monitoring

## Technology Stack

### Frontend
- **React 18** - Modern UI framework
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first styling
- **Lucide React** - Beautiful icons
- **Vite** - Fast build tool

### Backend
- **Supabase** - Backend-as-a-Service
  - PostgreSQL database
  - Authentication
  - Row Level Security (RLS)
  - Real-time subscriptions

## Getting Started

### Prerequisites
- Node.js 18+ and npm
- Supabase account

### Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   Create a `.env` file in the root directory with your Supabase credentials:
   ```
   VITE_SUPABASE_URL=your_supabase_url
   VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. The database schema has been automatically applied. Your Supabase database includes:
   - `profiles` - User profiles and information
   - `jobs` - Job postings
   - `events` - Events and meetups
   - `donations` - Donation records
   - `connections` - Alumni networking connections
   - `event_registrations` - Event RSVP tracking

5. Start the development server:
   ```bash
   npm run dev
   ```

6. Build for production:
   ```bash
   npm run build
   ```

## Project Structure

```
src/
├── components/        # Reusable components
│   └── Navigation.tsx # Main navigation bar
├── contexts/          # React contexts
│   └── AuthContext.tsx # Authentication state management
├── lib/              # Utility libraries
│   └── supabase.ts   # Supabase client and types
├── pages/            # Page components
│   ├── Landing.tsx          # Landing page
│   ├── Login.tsx            # Login page
│   ├── Register.tsx         # Registration page
│   ├── Dashboard.tsx        # User dashboard
│   ├── AlumniDirectory.tsx  # Alumni directory
│   ├── Jobs.tsx             # Job board
│   ├── Events.tsx           # Events management
│   ├── Donations.tsx        # Donation portal
│   ├── Profile.tsx          # User profile
│   └── Admin.tsx            # Admin dashboard
├── App.tsx           # Main application component
└── main.tsx          # Application entry point
```

## Database Schema

### Tables

- **profiles**: Extended user information (linked to auth.users)
- **jobs**: Job postings with company details
- **events**: Events with virtual/in-person support
- **event_registrations**: RSVP tracking
- **donations**: Donation records with campaign tracking
- **connections**: Alumni networking requests

All tables have Row Level Security (RLS) enabled for secure data access.

## Features by Role

### Alumni
- Full access to directory, jobs, events, donations
- Can post jobs and create events
- Update personal profile
- Connect with other alumni
- Offer mentorship

### Students
- Browse directory and connect with alumni
- View jobs and events
- Register for events
- Update personal profile

### Admins
- All alumni features
- Access to admin dashboard
- Platform analytics and statistics
- User management capabilities

## Responsive Design

The platform is fully responsive and optimized for:
- Desktop (1024px+)
- Tablet (768px - 1023px)
- Mobile (< 768px)

## Security

- Row Level Security (RLS) on all tables
- Authentication required for sensitive operations
- Role-based access control
- Secure password handling
- Protection against SQL injection and XSS

## Contributing

This project was built as a demonstration for a 24-hour hackathon challenge. Feel free to fork and customize it for your institution's needs.

## License

MIT License - Feel free to use this project for educational or commercial purposes.

## Support

For questions or issues, please open an issue in the repository.
