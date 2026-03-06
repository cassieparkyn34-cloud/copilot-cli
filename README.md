# GitHub Copilot CLI (Public Preview)

The power of GitHub Copilot, now in your terminal.

GitHub Copilot CLI brings AI-powered coding assistance directly to your command line, enabling you to build, debug, and understand code through natural language conversations. Powered by the same agentic harness as GitHub's Copilot coding agent, it provides intelligent assistance while staying deeply integrated with your GitHub workflow.

See [our official documentation](https://docs.github.com/copilot/concepts/agents/about-copilot-cli) for more information.

![Image of the splash screen for the Copilot CLI](https://github.com/user-attachments/assets/51ac25d2-c074-467a-9c88-38a8d76690e3)

## 🚀 Introduction and Overview

We're bringing the power of GitHub Copilot coding agent directly to your terminal. With GitHub Copilot CLI, you can work locally and synchronously with an AI agent that understands your code and GitHub context.

- **Terminal-native development:** Work with Copilot coding agent directly in your command line — no context switching required.
- **GitHub integration out of the box:** Access your repositories, issues, and pull requests using natural language, all authenticated with your existing GitHub account.
- **Agentic capabilities:** Build, edit, debug, and refactor code with an AI collaborator that can plan and execute complex tasks.
- **MCP-powered extensibility:** Take advantage of the fact that the coding agent ships with GitHub's MCP server by default and supports custom MCP servers to extend capabilities.
- **Full control:** Preview every action before execution — nothing happens without your explicit approval.

We're still early in our journey, but with your feedback, we're rapidly iterating to make the GitHub Copilot CLI the best possible companion in your terminal.

## 📦 Getting Started

### Supported Platforms

- **Linux**
- **macOS**
- **Windows**

### Prerequisites

- **Node.js** v22 or higher
- **npm** v10 or higher
- (On Windows) **PowerShell** v6 or higher
- An **active Copilot subscription**. See [Copilot plans](https://github.com/features/copilot/plans?ref_cta=Copilot+plans+signup&ref_loc=install-copilot-cli&ref_page=docs).

If you have access to GitHub Copilot via your organization of enterprise, you cannot use GitHub Copilot CLI if your organization owner or enterprise administrator has disabled it in the organization or enterprise settings. See [Managing policies and features for GitHub Copilot in your organization](http://docs.github.com/copilot/managing-copilot/managing-github-copilot-in-your-organization/managing-github-copilot-features-in-your-organization/managing-policies-for-copilot-in-your-organization) for more information.

### Installation

Install globally with npm:
```bash
npm install -g @github/copilot
```

### Launching the CLI

```bash
copilot
```

On first launch, you'll be greeted with our adorable animated banner! If you'd like to see this banner again, launch `copilot` with the `--banner` flag. 

If you're not currently logged in to GitHub, you'll be prompted to use the `/login` slash command. Enter this command and follow the on-screen instructions to authenticate.

#### Authenticate with a Personal Access Token (PAT)

You can also authenticate using a fine-grained PAT with the "Copilot Requests" permission enabled.

1. Visit https://github.com/settings/personal-access-tokens/new
2. Under "Permissions," click "add permissions" and select "Copilot Requests"
3. Generate your token
4. Add the token to your environment via the environment variable `GH_TOKEN` or `GITHUB_TOKEN` (in order of precedence)

### Using the CLI

Launch `copilot` in a folder that contains code you want to work with. 

By default, `copilot` utilizes Claude Sonnet 4.5. Run the `/model` slash command to choose from other available models, including Claude Sonnet 4 and GPT-5

Each time you submit a prompt to GitHub Copilot CLI, your monthly quota of premium requests is reduced by one. For information about premium requests, see [About premium requests](https://docs.github.com/copilot/managing-copilot/monitoring-usage-and-entitlements/about-premium-requests).

For more information about how to use the GitHub Copilot CLI, see [our official documentation](https://docs.github.com/copilot/concepts/agents/about-copilot-cli).


## 💡 Example Use Cases

GitHub Copilot CLI can help you build a wide range of applications. Here are a few examples to get you started:

### 📚 Book App

Build a reading or book management app — for example, a personal library tracker where you can catalog books, track reading progress, and write reviews:

```
> Create a book app where I can track books I'm reading, mark them as read or unread, and add personal notes for each book. Use a simple web interface with a database to persist the data.
```

Copilot CLI will scaffold the project, create the necessary files, set up a database schema, and wire up the UI — all through natural language conversation.

### 🌐 Web App

Build full-stack web applications quickly. For example, start a new React + Node.js project:

```
> Create a web app with a React frontend and an Express backend. Include user authentication, a home page, and a dashboard. Use Tailwind CSS for styling.
```

You can iterate on the design, add features, and fix bugs all within the same Copilot CLI session.

### 🎬 Video Editing Tool

Build a video editing or processing application. For example, a tool that trims, merges, or adds subtitles to videos:

```
> Create a video editing tool that lets me trim video clips, merge multiple videos together, and export the result. Use ffmpeg for the video processing and provide a simple command-line interface.
```

Copilot CLI will help set up the project dependencies, write the processing logic, and create the CLI interface for your video editor.

### 🍽️ Meal Planning App

Build an easy meal planning app to organize your weekly meals, generate shopping lists, and discover new recipes:

```
> Create a simple meal planning app where I can plan meals for each day of the week, add recipes with ingredients, and automatically generate a shopping list based on my weekly plan. Keep it easy to use with a clean web interface.
```

Copilot CLI will set up the project, create a recipe and meal plan data model, build the weekly planner UI, and wire up the shopping list generator — making meal planning effortless.

---

## 📢 Feedback and Participation

We're excited to have you join us early in the Copilot CLI journey.

This is an early-stage preview, and we're building quickly. Expect frequent updates--please keep your client up to date for the latest features and fixes!

Your insights are invaluable! Open issue in this repo, join Discussions, and run `/feedback` from the CLI to submit a confidential feedback survey!
