```markdown
# Crew-AI: Automated Blog Generation from YouTube

## Description
This project leverages [CrewAI] to create an AI-driven crew of agents that:
- **Research** Black Hole.
- **Generate blog content** from the video content automatically.

The system consists of:
- **Agents**: Specialized AI roles (Researcher, Writer)
- **Tasks**: Researching videos and writing blogs
- **Tools**: YouTube search and channel-specific search tools

---

## Project Structure
```

Crew-AI/
│-- crew\.py        # Initializes the crew and executes tasks
│-- agents.py      # Defines AI agents (Researcher & Writer)
│-- tasks.py       # Defines tasks for the agents
│-- tools.py       # YouTube search tools configuration
│-- requirements.txt
│-- .gitignore

````

---

## Requirements
```bash
python>=3.10
crewai
crewai_tools
python-dotenv
openai
````

---

## Installation

```bash
# Clone the repository
git clone https://github.com/AmitS1009/R-W-Ai-Agent.git
cd R-W-Ai-Agent

# Create virtual environment
python -m venv myvenv
source myvenv/bin/activate   # On Linux/Mac
myvenv\Scripts\activate      # On Windows

# Install dependencies
pip install -r requirements.txt
```

---

## Environment Setup

Create a `.env` file in the project root:

```env
OPENAI_API_KEY=your_openai_api_key_here
```

---

## How It Works

1. **crew\.py** creates a Crew with:

   * `blog_researcher` agent: Searches YouTube channel for relevant video transcripts.
   * `blog_writer` agent: Writes a structured blog post based on research.
2. **tasks.py** defines:

   * `research_task`: Extracts content from YouTube.
   * `write_task`: Converts extracted data into a blog post (`new-blog-post.md`).
3. **tools.py** provides:

   * `yt_tool`: Searches within `@SabineHossenfelder` YouTube channel.

---

## Run the Project

```bash
python crew.py
```

Output:

* Generates a blog post in `new-blog-post.md`
* Prints execution results in the terminal

---

## Example Command & Output

```bash
python crew.py
```

```plaintext
Executing tasks...
Researching topic: Whats there inside Black Hole
Generating blog content...
Blog post saved to new-blog-post.md
```

---

## License

```text
Apache-2.0 license
```

```
```
