# 🧠 AI Job Application Assistant (CrewAI)

This project is an intelligent agent-based pipeline using [CrewAI](https://docs.crewai.com/) to automate and enhance the job application process for engineering roles. It leverages advanced tools and LLMs to analyze resumes, research job postings, and prepare candidates for interviews.

---

## 🚀 Key Features

- 🔍 **Job Market Research**: Automatically scrape and analyze job listings to extract relevant skills and requirements.
- 👤 **Applicant Profiling**: Read and semantically analyze resumes to create detailed applicant profiles.
- 📝 **Resume Optimization**: Suggest improvements to tailor resumes according to job demands.
- 🎤 **Interview Preparation**: Generate personalized interview questions and preparation strategies.

---

## 🧩 Components & Agents

The application uses four main AI agents:

1. **Tech Job Researcher**  
   - Scrapes and analyzes job listings.  
   - Extracts required qualifications and trends.

2. **Personal Profiler**  
   - Reads resumes (`fake_resume.md`).  
   - Builds a candidate profile using semantic search.

3. **Resume Strategist**  
   - Suggests how to tailor resumes to match job roles.  
   - Ensures skills and experiences are properly highlighted.

4. **Interview Preparer**  
   - Generates interview questions and tips.  
   - Simulates potential questions based on job listings.

Each agent is instantiated using `crewai.Agent` and uses tools from `crewai_tools` such as:

- `SerperDevTool`: For search  
- `ScrapeWebsiteTool`: For scraping job websites  
- `FileReadTool` and `MDXSearchTool`: For reading and searching within resumes

---

## 🛠️ Requirements

Install dependencies using:

```bash
pip install crewai==0.28.8 crewai_tools==0.1.6 langchain_community==0.0.29
```

Also ensure:

- You have valid API keys for:
  - TogetherAI (`TOGETHER_API_KEY`)
  - Serper.dev (`SERPER_API_KEY`)
- You provide a resume file at `./fake_resume.md`.

---

## 📂 Project Structure

```
.
├── main.py               # Main script to run the crew-based job assistant
├── utils.py              # Contains functions to load API keys
├── fake_resume.md        # Markdown file with applicant’s resume
├── README.md             # You're here!
```

---

## 🧪 How to Run

1. Set your API keys in `utils.py` or environment variables.
2. Ensure `fake_resume.md` exists in the root directory.
3. Run:

```bash
python main.py
```

The program will:
- Analyze the resume
- Scrape current job postings
- Suggest resume improvements
- Generate interview preparation materials

---

## 📈 Output

- Console logs showing each agent’s actions and insights.
- Improved resume suggestions and interview questions.

---

## 📌 Notes

- Designed primarily for **engineers**, but extendable to other fields.
- Demo resume used is `fake_resume.md` – replace it with real data for actual use.
- Follows modular architecture – easy to plug in new agents/tools.

---

## 📚 References

- [CrewAI Docs](https://docs.crewai.com/)
- [LangChain Community](https://python.langchain.com/)
- [Together AI](https://www.together.ai/)
- [Serper.dev](https://serper.dev/)
