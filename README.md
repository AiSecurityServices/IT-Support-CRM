<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# IT Support CRM - Task & Project Manager

A modern IT Support Customer Relationship Management system with AI-powered features for managing tasks, projects, and customer interactions.

🌐 **Live Demo:** [https://muhibchy.github.io/IT-Support-CRM/](https://muhibchy.github.io/IT-Support-CRM/)

## Features

- 📊 Dashboard with analytics and insights
- 📝 Task and project management
- 🤖 AI-powered assistance with Gemini API
- 📈 Performance tracking with charts
- 🎨 Modern, responsive UI with TailwindCSS

## Run Locally

**Prerequisites:** Node.js (v18 or higher)

1. **Clone the repository:**
   ```bash
   git clone https://github.com/MuhibChy/IT-Support-CRM.git
   cd IT-Support-CRM
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Set up environment variables:**
   - Copy `.env.local.example` to `.env.local`
   - Get your Gemini API key from [Google AI Studio](https://aistudio.google.com/app/apikey)
   - Add your API key to `.env.local`:
     ```
     GEMINI_API_KEY=your_api_key_here
     ```

4. **Run the development server:**
   ```bash
   npm run dev
   ```

5. **Open your browser:**
   Navigate to `http://localhost:3000`

## Deploy to GitHub Pages

This project is configured for automatic deployment to GitHub Pages.

### Setup Instructions:

1. **Enable GitHub Pages:**
   - Go to your repository Settings
   - Navigate to Pages section
   - Under "Source", select **GitHub Actions**

2. **Add API Key Secret:**
   - Go to Settings > Secrets and variables > Actions
   - Click "New repository secret"
   - Name: `GEMINI_API_KEY`
   - Value: Your Gemini API key
   - Click "Add secret"

3. **Deploy:**
   - Push to the `main` branch, or
   - Go to Actions tab and manually trigger "Deploy to GitHub Pages"

4. **Access your site:**
   Your app will be live at: `https://[your-username].github.io/IT-Support-CRM/`

## Build for Production

```bash
npm run build
```

The built files will be in the `dist` folder.

## Tech Stack

- **Frontend:** React 19, TypeScript
- **Styling:** TailwindCSS
- **Charts:** Recharts
- **Build Tool:** Vite
- **AI:** Google Gemini API
- **Deployment:** GitHub Pages

## Project Structure

```
IT-Support-CRM/
├── components/        # React components
├── data/             # Data models and utilities
├── .github/          # GitHub Actions workflows
├── App.tsx           # Main application component
├── index.tsx         # Application entry point
├── types.ts          # TypeScript type definitions
└── vite.config.ts    # Vite configuration
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the MIT License.
