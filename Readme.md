# GitHub PR Review AI

**GitHub PR Review AI** is a sophisticated web application designed to deliver AI-powered code reviews for GitHub pull requests. By leveraging advanced language models, this tool provides developers with immediate, high-quality feedback on code changes, reducing dependency on human reviewers and accelerating the development process.

![GitHub PR Review AI Screenshot](https://placeholder.svg?height=400&width=800)

## Key Features

- **AI-Driven Code Analysis**: Receive detailed feedback on code style, security vulnerabilities, performance optimizations, and design patterns.
- **Seamless GitHub Integration**: Effortlessly retrieve pull request diffs from any public GitHub repository.
- **Automated Comment Posting**: Optionally post AI-generated reviews as comments directly on GitHub pull requests.
- **Formatted Feedback**: Render reviews in beautifully formatted markdown with syntax-highlighted code snippets.
- **Responsive Interface**: Access the application on both desktop and mobile devices.
- **Theme Support**: Toggle between light and dark modes for an optimal viewing experience.

## Installation

### Prerequisites

To set up the application, ensure you have the following:

- **Node.js**: Version 18.x or higher
- **Package Manager**: npm or Yarn
- **GitHub Personal Access Token**: With `repo` scope permissions
- **LLM API Access**: Access to Gaia LLM or a compatible large language model API

### Setup Instructions

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/github-pr-review-ai.git
   cd github-pr-review-ai
   ```

2. **Install Dependencies**:

   ```bash
   npm install
   # or
   yarn install
   ```

3. **Configure Environment Variables**:

   Create a `.env.local` file in the project root and add the following variables:

   ```env
   GITHUB_TOKEN=your_github_personal_access_token
   GAIA_API_KEY=your_gaia_api_key
   GAIA_API_BASE_URL=your_gaia_api_base_url
   GAIA_MODEL=gpt-4o  # Optional: Specify your preferred model
   ```

4. **Start the Development Server**:

   ```bash
   npm run dev
   # or
   yarn dev
   ```

5. **Access the Application**:

   Open your browser and navigate to [http://localhost:3000](http://localhost:3000).

## Usage

To perform a code review:

1. Enter the GitHub repository owner (username or organization).
2. Specify the repository name.
3. Provide the pull request number.
4. (Optional) Enable the "Post review as a GitHub comment" option to share the review on the pull request.
5. Click **Review Pull Request**.
6. Wait for the AI to analyze the code changes.
7. Review the generated feedback, presented in a clear and structured format.

## Environment Variables

| Variable              | Description                                      | Required |
|-----------------------|--------------------------------------------------|----------|
| `GITHUB_TOKEN`        | GitHub Personal Access Token with repo access    | Yes      |
| `GAIA_API_KEY`        | API key for Gaia LLM                             | Yes      |
| `GAIA_API_BASE_URL`   | Base URL for Gaia API                            | Yes      |
| `GAIA_MODEL`          | LLM model name (defaults to `gpt-4o`)            | No       |

## Technology Stack

The application is built using modern, industry-standard technologies:

- **Next.js**: A full-stack React framework for server-side rendering and static site generation.
- **TypeScript**: Enhances JavaScript with static typing for improved reliability.
- **Tailwind CSS**: A utility-first CSS framework for rapid UI development.
- **shadcn/ui**: Reusable, high-quality UI components.
- **React Hook Form**: Efficient form handling and validation.
- **Zod**: Schema validation for robust data integrity.
- **LangChain**: Simplifies integration with large language models.
- **React Markdown**: Renders markdown content with rich formatting.
- **React Syntax Highlighter**: Provides syntax highlighting for code snippets.

## Project Structure

```plaintext
github-pr-review-ai/
├── app/
│   ├── actions.ts        # Server-side actions for pull request reviews
│   ├── globals.css       # Global CSS styles
│   ├── layout.tsx        # Application root layout
│   └── page.tsx          # Main application page
├── components/
│   ├── review-form.tsx   # Pull request review form component
│   ├── theme-provider.tsx # Theme management for light/dark modes
│   └── ui/               # Reusable UI components
├── lib/
│   └── utils.ts          # Utility functions
├── public/
│   └── ...               # Static assets
├── .env.local            # Environment variables (not tracked in git)
├── next.config.js        # Next.js configuration
├── package.json          # Project dependencies and scripts
├── README.md             # Project documentation
└── tsconfig.json         # TypeScript configuration
```

## How It Works

The application operates through the following workflow:

1. **Input Collection**: Users provide repository details and the pull request number.
2. **GitHub API Integration**: The application fetches the pull request diff via the GitHub API.
3. **AI Analysis**: The diff is processed by the Gaia LLM for comprehensive analysis.
4. **Feedback Generation**: The AI produces structured, actionable feedback.
5. **Comment Posting (Optional)**: Feedback can be posted as a comment on the pull request.
6. **Rendering**: Feedback is displayed in formatted markdown with syntax highlighting.

## Planned Enhancements

Future improvements to the application may include:

- Integration with GitHub OAuth for simplified authentication.
- Persistent storage for review history.
- A visual diff viewer for enhanced code comparison.
- Customizable review templates for tailored feedback.
- Support for private repositories.

## Contributing

We welcome contributions from the community. To contribute:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/amazing-feature`).
3. Commit your changes (`git commit -m 'Add some amazing feature'`).
4. Push to the branch (`git push origin feature/amazing-feature`).
5. Open a pull request for review.

Please ensure your contributions adhere to the project's coding standards and include appropriate documentation.

## License

This project is licensed under the [MIT License](LICENSE). See the LICENSE file for details.

## Acknowledgements

We extend our gratitude to the following projects and communities:

- [Next.js](https://nextjs.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [shadcn/ui](https://ui.shadcn.com/)
- [GitHub API](https://docs.github.com/en/rest)
- [LangChain](https://js.langchain.com/)

