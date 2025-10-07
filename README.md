# AI-Email-Agent-n8n
AI-powered email management workflow built with n8n

## 🧠 Built My Own AI Email Agent Using n8n + OpenAI

Handling emails used to be one of the most frustrating parts of my day. My inbox was constantly overflowing with promotions, social updates, job notifications, receipts, and random newsletters. It was almost impossible to spot what was truly important — a client message, a job update, or a personal email.

So, I decided to create something smart — an **AI-powered Email Agent** that reads, classifies, labels, and organizes my inbox automatically.
Now, instead of me cleaning my inbox, the AI does it for me.

### ⚡ 1. The Idea

I wanted to build a workflow that could:

* Understand the type of each email — distinguish between Promotions, Social, Recruitment, Sales, Personal, and Receipts.
* Automatically create Gmail labels for each category.
* Log every processed email (sender, subject, category, timestamp) into a Google Sheet for tracking and analytics.
* Handle recruitment emails separately — flag them, highlight them, and store them in a special section.
* Keep my inbox clean and prioritized — so I see only what really matters.

I wanted to combine AI intelligence with workflow automation to handle something everyone struggles with: email overload.


### ⚙️ 2. How I Built It

#### 🧩 Step 1: The Foundation — n8n

I used n8n as my automation tool. It’s open-source, visual, and lets me design flows without deep coding.

My flow begins with a Gmail Trigger — it activates automatically whenever a new email arrives in my inbox.

#### 🧠 Step 2: The Brain — OpenAI

Once the email arrives, I send its subject and body text to OpenAI’s model through the OpenAI Node.

I designed a custom prompt that tells the AI to classify the email into one of several categories:

* Promotions
* Social
* Recruitment
* Sales
* Personal
* Receipts
* Scam / Spam / Unwanted

This part took time — I tested different prompts, adjusted parameters, and even added rules to make sure emails like invoices and job offers were always categorized correctly.

#### ⚙️ Step 3: Smart Actions

After classification, the workflow performs multiple actions depending on the category:

* Promotions / Social → Archived or labeled automatically to declutter my inbox.
* Scam / Spam → Deleted permanently using Gmail’s delete node.
* Receipts / Transactions → Logged into a Google Sheet for record-keeping and monthly expense tracking.
* Recruitment / Job mails → Highlighted and stored in a separate “Recruitment” label for easy review.
* Important / Personal → Triggers a notification pop-up so I don’t miss it.

I also experimented with adding an auto-reply generator using OpenAI — it drafts polite responses for professional or recruitment emails.


### 📊 3. Logging & Analytics

Every email processed gets logged into **Google Sheets** with columns for:

* Sender
* Subject
* Category
* Timestamp
* Action Taken

This allows me to analyze patterns later — like how many spam vs. important emails I get per week.

### 🧰 Tech Stack

* n8n – Workflow automation engine
* OpenAI API – For intelligent text classification
* Gmail API – For fetching, labeling, and managing emails
* Google Sheets API – For Summary and analytics

Because this project is more than automation — it’s proof that AI + no-code tools can work together to simplify real-life problems.

This build taught me:

* How to design prompt-based classifiers that handle messy data like emails.
* How to connect APIs between Gmail, Google Sheets, and OpenAI using n8n.
* How automation can save hours of manual sorting and improve focus every day.


### 🏁 Final Thoughts

Sometimes, the best AI projects aren’t the most complex — they’re the ones that make your own life easier.

This AI Email Agent doesn’t just automate — it thinks, classifies, and acts intelligently, keeping my inbox neat and my attention focused.


