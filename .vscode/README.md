# VS Code Development Setup

## Quick Start

Press `F5` or go to **Run and Debug** (⇧⌘D) and select:

- **Rails + Webpack (Full Stack)** - Recommended: Runs both Rails server and webpack-dev-server

Your application will be available at: http://localhost:3000

## Available Launch Configurations

1. **Rails Server** - Start Rails server only on port 3000
2. **Rails Console** - Open an interactive Rails console
3. **Rails + Webpack (Full Stack)** - Start both Rails and webpack dev server

## Available Tasks

Access via **Terminal → Run Task** (⇧⌘P → "Tasks: Run Task"):

- **Start Webpack Dev Server** - Run webpack dev server separately
- **Start Sidekiq** - Start background job processor (requires Redis)
- **Run Tests** - Execute the test suite

## Prerequisites Installed

✅ Ruby 3.2.3 (via rbenv)
✅ PostgreSQL 15
✅ Node.js 22.13.0 (via nvm)
✅ Yarn 1.22.22
✅ All gem dependencies
✅ All npm dependencies
✅ Database created and schema loaded

## Optional: Install Redis (for background jobs)

```bash
brew install redis
brew services start redis
```

Then you can run Sidekiq via the task menu.

## Database Commands

```bash
bundle exec rails db:migrate    # Run migrations
bundle exec rails db:seed       # Seed database
bundle exec rails db:reset      # Reset database
```

## Troubleshooting

If the server doesn't start:

1. Make sure PostgreSQL is running: `brew services list`
2. Check the `.env` file has correct database credentials
3. Verify dependencies: `bundle install && yarn install`
