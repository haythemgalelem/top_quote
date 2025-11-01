<h1>🧠 Top Quote</h1>

<p>Automatically collected and stored quotes — one quote at a time.</p>

<p>This repository is maintained and updated automatically using <a href="https://n8n.io/">n8n</a>, a workflow automation tool, to save inspiring, thought-provoking, or stylistic quotes as JSON files, organized by date.</p>

<h2>📂 Repository Structure</h2>
<pre>
top_quote/
├── 2025-11-01/
│   ├── quote_1762026345123.json
│   ├── quote_1762026371924.json
│   ├── quote_1762026482695.json
│   ├── quote_1762026518711.json
│   └── quote_1762027033868.json
└── ...
</pre>

<h2>🧾 JSON File Format</h2>
<p>Each quote is saved in a simple JSON format:</p>
<pre>
{
  "value": "Style is genderless"
}
</pre>
<p><strong>value</strong> — the text content of the quote.</p>

<h2>🔄 Automation Workflow</h2>
<p>This repository is updated automatically using <strong>n8n</strong>, a low-code workflow automation tool.</p>
<p>The workflow steps:</p>
<ol>
    <li>Fetch or receive a quote from a source (API, RSS feed, manual input, etc.).</li>
    <li>Create a new JSON file named with a timestamp for uniqueness.</li>
    <li>Commit and push the new file to the GitHub repository under a folder named with the current date (<code>YYYY-MM-DD</code>).</li>
</ol>

<h2>💡 Use Cases</h2>
<ul>
    <li>Build a <strong>Quote of the Day</strong> feature for websites or apps.</li>
    <li>Source content for social media posts or newsletters.</li>
    <li>Gather datasets for natural language processing or sentiment analysis.</li>
    <li>Maintain a personal or public inspirational quote archive.</li>
</ul>

<h2>🛠️ Usage Examples</h2>

<h3>JavaScript</h3>
<pre>
fetch('https://raw.githubusercontent.com/haythemgalelem/top_quote/main/2025-11-01/quote_1762026345123.json')
  .then(res =&gt; res.json())
  .then(data =&gt; console.log(data.value));
</pre>

<h3>Python</h3>
<pre>
import requests

url = "https://raw.githubusercontent.com/haythemgalelem/top_quote/main/2025-11-01/quote_1762026345123.json"
quote = requests.get(url).json()
print(quote["value"])
</pre>

<h2>🗓️ Naming Convention</h2>
<ul>
    <li><strong>Folder:</strong> Date formatted as <code>YYYY-MM-DD</code></li>
    <li><strong>File:</strong> <code>quote_&lt;timestamp&gt;.json</code>, where <code>&lt;timestamp&gt;</code> is a unique numeric identifier</li>
</ul>

<h2>🤝 Contributing</h2>
<p>While the repository is mainly automated, contributions are welcome! You can help by:</p>
<ul>
    <li>Suggesting or integrating new quote sources.</li>
    <li>Adding metadata fields to enrich quotes (author, tags, etc.).</li>
    <li>Improving automation workflows.</li>
    <li>Fixing formatting or improving documentation.</li>
</ul>

<p>To contribute:</p>
<ol>
    <li>Fork the repository.</li>
    <li>Create a feature branch: <code>git checkout -b feature-name</code></li>
    <li>Commit your changes: <code>git commit -m "Describe your changes"</code></li>
    <li>Push to your branch: <code>git push origin feature-name</code></li>
    <li>Open a Pull Request and describe your enhancements.</li>
</ol>

<h2>📜 License</h2>
<p>This project is licensed under the <strong>MIT License</strong>. See the <code>LICENSE</code> file for details.</p>

<h2>👤 Maintainer</h2>
<p>Created and maintained by <a href="https://github.com/haythemgalelem">@haythemgalelem</a><br>
Automated with ❤️ using <a href="https://n8n.io/">n8n</a></p>

<h2>📖 Optional: Rebuilding the Automation</h2>
<p>If you'd like to run your own automation to populate quotes, you can set up an n8n workflow with these components:</p>
<ul>
    <li><strong>Trigger:</strong> Schedule trigger or webhook.</li>
    <li><strong>Quote Fetcher:</strong> HTTP request or custom node to get quotes.</li>
    <li><strong>File Writer:</strong> Write quote JSON to local filesystem or push to GitHub.</li>
    <li><strong>GitHub Commit:</strong> Use GitHub API node to commit the new JSON file.</li>
</ul>
<p>This workflow ensures continuous, organized collection of quotes with minimal manual effort.</p>

<p>Thank you for exploring the Top Quote project! Feel free to star, fork, or contribute.</p>

</body>
</html>
