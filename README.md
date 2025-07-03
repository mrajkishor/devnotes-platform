
# DevNotes Platform

A learning site built to organize and share technical knowledge in web development, computer science, and data science.

The project aims to make it easier for students and job-seeking developers to find clean, concise explanations without noise or distractions. Content is served from AWS, loaded dynamically by URL, and kept fast with caching.

---

## Who It's For

- BTech / MCA students who want clear, structured notes
- Anyone upskilling in full stack, CS fundamentals, or machine learning

---

## Topics Covered

### Full Stack
- HTML, CSS, JS basics
- React, Node, Express, REST APIs
- MongoDB, PostgreSQL
- Git, Docker etc.

### Computer Science
- Operating Systems
- DBMS
- Networking
- DSA, Algorithms, OOP etc.

### Data Science & AI
- Python for data
- Statistics & probability
- Machine learning
- Scikit-learn, pandas, NumPy etc.

---

## How It Works

- The frontend is built with Next.js and deployed on Vercel
- Each URL (like `/os/scheduling`) is mapped to a Markdown file ID
- A backend (AWS Lambda) looks up the ID using DynamoDB
- Then fetches the file from S3 and returns it
- The returned file is rendered on the client
- AdSense is used for monetization

---

## Example URLs

```

/full-stack/react/state-vs-props
/computer-science/dbms/indexing
/data-science/ml/k-means

````

---

## Stack

- **Frontend**: Next.js + React
- **Content**: Files like .doc, .pdf, .txt, .md, .jpg, .webp etc.
- **Backend**: AWS Lambda + API Gateway
- **Mapping**: DynamoDB (URL to file ID)
- **Storage**: S3
- **Deployment**: Vercel (UI), AWS (API)
- **Logging**: CloudWatch
- **Ads**: Google AdSense


![Untitled-2025-06-23-0040](https://github.com/user-attachments/assets/e0296b7d-68a8-40ee-96aa-bff86035fcd5)



---

## Things I'm Still Improving

- Adding a basic search function
- Auto-generating sitemap and topic lists
- Bookmarking feature
- Better topic hierarchy display
- Possible login + dashboard for readers later

---

## Dev Setup

```bash
git clone https://github.com/mrajkishor/devnotes-platform
cd devnotes-platform
npm install
npm run dev
````

Make sure to set up your `.env` with S3 and API keys.

---

## License

MIT – use, share, or build on it.

---

> This project is part learning tool, part knowledge dump, and part portfolio. If it helps anyone, that’s enough for me.
