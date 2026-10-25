# Competitor Monitoring Alert Tool

An automated competitor monitoring tool built with **n8n Cloud** that tracks competitor pricing and discovers newly published blog posts, sending email alerts when relevant changes are detected.

## Live Demo

**Try the tool:** https://parthgairola5.app.n8n.cloud/form/14ea0162-d5b2-4aea-8e22-bb9f727d8efd

Enter a competitor domain and your email address to run the monitoring workflow.

## Workflow Overview

<!-- Add your full workflow screenshot below this line -->
<img width="1612" height="585" alt="image" src="https://github.com/user-attachments/assets/dabf02fc-e387-49d3-9ba6-6902cdbbc765" />

*Complete n8n workflow showing the Pricing Monitor and Content Monitor.*

## Features

### 1. Pricing Monitor
- Fetches a competitor's pricing page.
- Extracts and compares prices with a previously saved snapshot.
- Stores pricing data in n8n Data Tables.
- Sends email alerts when pricing changes are detected.

### 2. Content Monitor
- Fetches sitemap data to discover blog posts.
- Falls back to blog-page links and RSS feeds when needed.
- Extracts article titles, descriptions, publication dates, and URLs.
- Compares discovered posts against previously saved records.
- Generates target keywords from new article titles.
- Sends email alerts for new posts or when no new posts are found.

### 3. Web Form
- Accepts a competitor domain and email address.
- Runs both monitoring workflows from a single submission.
- Displays a completion message after the workflow finishes.

## Screenshots

### Submission Form

<img width="772" height="747" alt="image" src="https://github.com/user-attachments/assets/ce9417d1-ff02-4355-8bd8-8a5700ec6e11" />

### Email Alert Example

<img width="772" height="456" alt="image" src="https://github.com/user-attachments/assets/b1b0c8d2-500b-4d78-9d76-92484988e5f3" />
<img width="716" height="377" alt="image" src="https://github.com/user-attachments/assets/70fb3b7d-8c85-4325-8bee-f15f023d6310" />

## Tech Stack

- **Automation:** n8n Cloud
- **Web interface:** n8n Form Trigger
- **Web scraping:** HTTP Request and HTML extraction
- **Data storage:** n8n Data Tables
- **Processing:** JavaScript
- **Notifications:** Gmail
- **Data sources:** Website sitemaps, blog pages, and RSS feeds

## How It Works

1. The user submits a competitor domain and email address.
2. The workflow runs the pricing and content monitoring branches in parallel.
3. Pricing data is compared with the previously saved snapshot.
4. Blog posts are discovered, extracted, and checked against saved URLs.
5. Relevant email alerts are generated and sent.
6. The form displays a completion message when the workflow finishes.

## Setup

1. Download the workflow JSON from this repository.
2. Import it into an n8n instance.
3. Configure the required Gmail credentials and data tables.
4. Verify the node configurations and website accessibility.
5. Publish the workflow and open its production form URL.

## Limitations

- Some websites block automated requests or use JavaScript-rendered content.
- Pricing extraction currently focuses on dollar-denominated prices and may require adjustments for other formats.

## Author

**Parth Gairola**

[GitHub Profile](https://github.com/Parthgairola)

---
