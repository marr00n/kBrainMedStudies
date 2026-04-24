> [!NOTE] My Thoughts
> This is an interesting article that talks about how to create a dashboard to see what is going on in your business.
>
> An astute commenter noted that it's also helpful to maintain a decision log where you see what decisions you made and why that you review on a regular basis as this helps inform when you are making mistakes.

---
# Content


In the early days, you don't think of operations. You're just focused on building and shipping.

Over time, things build up. Tasks, content, leads, and requests are all in different places. Your memory may not cut it anymore.

Here’s how to build something that shows what’s going on and what needs your attention.

## What you’re building

A simple system: Input → Inbox → Tasks → Review

- Input = new things coming in
- Inbox = one place for all of them
- Tasks = work to do
- Review = decide what to focus on

## Tools (each has one job)

- **Notion** → dashboard (where you see everything)
- **Jotform** → input
- **Google Sheets** → leads and numbers
- **Zapier** → connects tools
- **ChatGPT** (or similar) → helps you decide

## Step 1 — Define your 5 streams

For most founders, that would be something like:

- Tasks
- Content
- Updates
- Leads
- Reporting

## Step 2 — Assign one home for each

- Tasks → Notion
- Content → Notion
- Updates → Notion (via Jotform input)
- Leads → Google Sheets
- Reporting → Google Sheets

Rule: one thing = one place

## Step 3 — Set up Tasks (Notion)

Go to Notion → create page: Mission Control

Create /table inline

Fields:

- Task name
- Status (To do / Doing / Done)
- Priority (Low / Medium / High)
- Due date

**Create your working view**

Click Filter

Add:

- Status = Doing OR
- Due date = today

Rename this view: Today

## Step 4 — Set up Content (Notion)

Create another table:

Fields:

- Title
- Status (Idea / Draft / Published)
- Channel
- Publish date

## Step 5 — Set up Updates (Jotform → Notion)

This is your input system.

### Create the form (Jotform)

Add:

- Title
- Details
- Type (Idea / Issue / Request / Update)
- Urgency
- Area (Tasks / Content / Leads / Other)

Publish the form.

### Create Updates table (Notion)

Fields:

- Title
- Type
- Urgency
- Area
- Created time

### Connect both using Zapier

- Trigger → Jotform: New submission
- Action → Notion: Create database item

Map fields:

- Title → Title
- Type → Type
- Urgency → Urgency
- Area → Area

### Test it

Submit the form.

Check Notion.

You should see a new row.

## Step 6 — Turn inputs into work

When something shows up in Updates:

- Look at each one and ask yourself: “does this need action?”

If something needs action:

- Create a new Task
- Set:
	- Status
		- Priority
		- Due date

Flow: Jotform → Updates → Tasks

**Optional: Automate simple, repeated tasks**

If you find yourself creating the same type of task, you should automate it.

For example:

If Type = Request and Urgency = High → create a Task automatically

## Step 7 — Set up Leads and Reporting (Google Sheets)

### Leads sheet

- Name
- Email
- Source
- Status
- Value

**Automate lead capture**

If leads come from a form:

- Trigger → Jotform submission
- Action → Add a new row in Google Sheets

Now every lead is automatically saved.

### Reporting sheet

- Date
- Leads
- Revenue
- Content published

### Show both in Notion

- Type `/embed`
- Paste your Google Sheets link

## Step 8 — Build your mission control layout

Go back to Notion → Mission Control page.

Now, arrange your Notion page like this(top to bottom):

1. Tasks (Today view)
2. Updates (latest first)
3. Content
4. Leads (embedded Google Sheet)
5. Reporting (key numbers)

Now you can see the main parts of your business on one page.

**Optional: daily reminder**

If you forget to check this page:

- Set a daily reminder (Zapier, phone, or calendar)
- Link directly to your Mission Control page

## Step 9 — Use AI (start manual first)

Don’t automate this step just yet.

Do it by hand first. It helps you understand what’s going on.

### Weekly summary

Every week:

1. Go to Notion and copy:
	- Tasks
		- Updates
2. Go to Google Sheets and copy:
	- Leads
		- key numbers
3. Paste into ChatGPT (or similar LLM)

Prompt:

```
Summarize this week's business activity.

Highlight:
- Key progress
- Blockers
- Missed opportunities

Suggest top 3 priorities for next week.
```

### Daily planning

Every morning:

1. Copy your “Today” section.
2. Paste into ChatGPT:
```
What should I prioritize today, given these tasks? 
Identify:
- Most important tasks
- Quick wins
- Risks
```

### Blocker detection

Every few days, copy your Updates (from Jotform).

Paste into ChatGPT:

```
Find patterns in these updates.
What blockers or issues keep showing up?
```

### Plan next week

Copy:

- Tasks
- Updates

Ask:

```
What should I focus on next week?
```

This helps you think clearly, even if you’re working alone.

**Finally, automate when:**

- Tasks are clear
- Updates are consistent
- You know what you’re doing
- Your system works
- Your data is clean

If your data is messy, you are more likely to get bad results.

### How to automate

Use Zapier and OpenAI.

**Example: weekly summary**

**Step 1 — Trigger**

In Zapier:

- Set a schedule → every Friday

**Step 2 — Get your data**

Add steps to pull your Tasks and Updates from Notion, and your lead data from Google Sheets.

**Step 3 — Send to AI**

Add a ChatGPT (OpenAI) step in Zapier and send your prompt.

**Step 4 — Send result somewhere**

- Send to email
- Or save in Notion
- Or send to Slack

## Step 10 — Add recurring updates

You want input on a regular basis.

**Option 1: Daily review**

In Jotform:

Create a form and answer:

- What did you do?
- What is blocked?
- What is next?

Submit this daily.

**Option 2: Weekly review**

Create a form with:

- Wins
- Problems
- Numbers
- Focus for next week

This keeps your system up to date.

## Step 11 — Add views (in Notion)

Sometimes you don’t want to see everything at once.

You just want to focus. That’s what views are for.

For example, you can make a view that shows:

- Only issues or requests in Updates
- Only content
- Only high-priority tasks

**Example:** Tasks → Add view → filter Priority = High

Keep it simple. Only create views you will really use.

---
**References / Source**
- [How to see your entire business on one page](https://www.indiehackers.com/post/how-to-see-your-entire-business-on-one-page-9f5546aad5) - [[Indie Hackers]]
