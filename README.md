# Automated Blog Content Generation from YouTube Videos

This project automates the process of generating high-quality blog posts from YouTube videos using the **CrewAI framework**. By integrating domain-specific AI agents, tools, and task workflows, it simplifies the creation of technical content related to AI, Machine Learning, and Data Science.

## Features

- Extracts transcriptions from YouTube videos for specified topics.
- Crafts engaging and simplified blogs for complex technical topics.
- Leverages multi-agent collaboration for research and writing.
- Streamlines execution with sequential task processing.

## Technologies Used

- **[CrewAI Framework]** Multi-agent collaboration and task management.
- **OpenAI GPT-4 API**: For generating coherent and high-quality content.
- **YouTubeChannelSearchTool**: Extracts transcriptions and metadata from YouTube channels.
- **dotenv**: Secure handling of API keys and environment variables.


## Usage

### 1. Define Agents

Agents are defined to handle research and writing tasks:

- **Blog Researcher Agent**:
  - Role: Extract transcriptions for a given topic from a specific YouTube channel.
  - Uses the `yt_tool` to interface with YouTube.

- **Blog Writer Agent**:
  - Role: Transform research insights into engaging blog posts.
  - Ensures simplified and compelling narratives.



### 2. Execute the Workflow

Start the task execution process with a specific topic:

```python
result = crew.kickoff(inputs={'topic': 'AI VS ML VS DL vs Data Science'})
print(result)
```

### 4. Review the Output

The `result` contains the final blog post draft, ready for publication.

## Example

Here is an example of the workflow:

1. **Input Topic**: `"AI VS ML VS DL vs Data Science"`
2. **Research Task**: Extracts transcriptions from the YouTube channel.
3. **Write Task**: Produces a blog post with simplified narratives and technical insights.
4. **Output**: Engaging blog content based on the extracted transcriptions.

## File Structure

```plaintext
.
├── agents.py            # Defines the blog researcher and writer agents.
├── tools.py             # Contains the YouTube channel search tool.
├── crew.py              # Configures the Crew and workflow.
├── tasks.py             # Defines the research and write tasks.
├── requirements.txt     # Lists the required Python packages.
├── .env                 # Stores environment variables.
└── README.md            # Project documentation.
```
