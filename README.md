# InterviewMirror

InterviewMirror is a frontend-based mock interview practice platform designed for students preparing for placements, internships, and entry-level roles.

It helps users practise HR and behavioural interview questions in a timed environment, speak answers aloud, review recognised transcripts, and receive structured rule-based feedback.

---

## Problem Statement

Many students know interview questions but struggle to practise speaking answers in a realistic timed environment.

They may not know whether their answer is long enough, structured properly, relevant to the question, or filled with unnecessary filler words.

InterviewMirror provides a browser-based environment where students can prepare, practise, analyse, and improve.

---

## Main Features

- HR and Behavioural interview modes
- 30-second preparation time before each question
- 60-second answer time for each question
- Browser speech recognition for spoken-answer transcripts
- Random two-question mock interview sessions
- Transcript-based practice report
- Rule-based score calculation
- Feedback on answer completeness, relevance, structure, pace, and filler-word usage
- Question Bank for HR and Behavioural interview preparation
- Downloadable interview summary PDF
- User name included in the final report
- No login required
- Local browser storage using localStorage

---

## User Flow

```text
Question Bank (Optional)
        ↓
Choose Interview Type
        ↓
Allow Microphone Access
        ↓
Preparation Time
        ↓
Speak Answers During Timed Questions
        ↓
Transcript Analysis
        ↓
Practice Report and PDF Summary
```

---

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Web Speech API
- localStorage
- jsPDF for PDF summary generation

---

## How the Score Is Calculated

InterviewMirror uses browser speech recognition and rule-based analysis.

It does not judge a student’s intelligence, personality, or employability. The score is only a practice signal based on the recognised spoken transcript and answer timing.

| Metric | Weight | What It Checks |
|---|---:|---|
| Answer Completeness | 25% | Whether the answer contains enough recognised spoken words |
| Relevance Signals | 25% | Whether useful interview-related keywords appear in the answer |
| Answer Structure | 20% | Whether the answer includes organisation markers or STAR-method signals |
| Speaking Pace | 15% | Estimated words per minute based on transcript length and answer time |
| Filler-Word Control | 15% | Frequency of filler words such as “um”, “uh”, and “like” |

### Final Score Formula

```text
Final Score =
(Completeness × 0.25) +
(Relevance × 0.25) +
(Structure × 0.20) +
(Pace × 0.15) +
(Filler Control × 0.15)
```

If no speech is recognised, the project shows a score of 0 and informs the user to check microphone permission or try again in Google Chrome or Microsoft Edge.

---

## Question Bank

The Question Bank is an optional preparation section for students who want to review common interview questions before practising.

It includes:

- HR Questions
- Behavioural Questions
- What the interviewer checks
- Quick answer tips

Students can directly start a mock interview without using the Question Bank.

---

## Project Structure

```text
InterviewMirror/
│
├── index.html
├── setup.html
├── interview.html
├── analysis.html
├── report.html
├── question-bank.html
│
├── css/
│   └── style.css
│
└── README.md
```

---

## How to Run the Project

1. Download or clone the project.
2. Open the project folder in VS Code.
3. Run `index.html` using Live Server.
4. Use Google Chrome or Microsoft Edge for better speech recognition support.
5. Allow microphone permission when prompted.

---

## Limitations

- Speech recognition depends on browser support and microphone permission.
- The project uses rule-based transcript analysis, not advanced AI semantic evaluation.
- The score cannot verify factual correctness of an answer.
- No user authentication or cloud database is used in the current version.
- Reports are stored only in the user’s browser through localStorage.

---

## Future Scope

- User authentication
- Cloud database for attempt history
- Dashboard with progress charts
- Technical interview question categories
- AI-powered semantic answer feedback
- Company-specific interview preparation
- Role-based question sets
- Multiple interview difficulty levels

---

## Author

**Shantanu Katiyar**

Built as a student-focused interview preparation project.
