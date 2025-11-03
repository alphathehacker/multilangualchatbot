***

```markdown
# Multilingual Chatbot with Flask & ChatBee

This project is a simple web chatbot built with Python Flask. The chatbot interface is served as a single HTML page, with the ChatBee widget providing multilingual conversational capabilities.

## Features

- Python Flask project structure
- Single-page chatbot interface (`index.html`)
- Native ChatBee widget integration (floating button)
- Ready for deployment on Render.com or other cloud platforms

## Getting Started

### Prerequisites

- Python 3.7+
- `Flask` package (`pip install flask`)
- [Optional, for local deployment] `gunicorn` for production (`pip install gunicorn`)
- GitHub/GitLab/Bitbucket account for Render deployment

### Project Structure

```
your-flask-chatbot/
├── app.py
└── templates/
    └── index.html
└── README.md
```

### Installation

1. **Clone the repository:**
   ```
   git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
   cd YOUR-REPO
   ```

2. **Install dependencies:**
   ```
   pip install flask
   ```

3. **Project files:**
   - Place `app.py` in the repo root.
   - Place `index.html` inside a `templates` folder.

4. **Add your ChatBee embed script in `index.html`**  
   ```
   <script src="https://www.chatbees.ai/embed.js"
           aid="TFJF9N99"
           colname="new"
           logoUrl="https://www.chatbees.ai/chatbees_logo_favicon_white.svg"
           brandName="Chatbees"
           greetingMessage="Hello! How can I assist you?"
           thinkingHint="Bees are thinking..."
           messagePlaceholder="Type your message here"></script>
   ```

### Running Locally

```
python app.py
```
Visit [http://localhost:3000](http://localhost:3000) in your browser.

### Deploying to Render.com

1. Push your code to GitHub/GitLab/Bitbucket.
2. Create a **new “Web Service”** on Render.com.
3. Set the **Start Command** as:
   ```
   gunicorn app:app
   ```
4. Set the **build environment** to Python 3.

Your chatbot will be available at `https://your-app-name.onrender.com`.

## Customization

- Edit `index.html` to customize the UI look & feel.
- Change ChatBee widget attributes to update greeting, branding, or collection.

## Troubleshooting

- Make sure your `index.html` is inside the `templates` folder and has the correct ChatBee embed script.
- For backend API integration, add your own `/chat` endpoint in `app.py`.

## License

MIT License (or your preferred license)

---

**For further help:**  
- ChatBee documentation: [https://docs.chatbees.ai](https://docs.chatbees.ai)
- Render.com documentation: [https://render.com/docs/static-sites](https://render.com/docs/static-sites) / [https://render.com/docs/deploy-flask](https://render.com/docs/deploy-flask)
```
