# bairwa-mahasabha-tonk
Official website for Bairwa Mahasabha Tonk, Rajasthan — built with HTML, CSS &amp; JavaScript. Features member registration, leadership showcase &amp; community resources.
# 🌐 Bairwa Mahasabha Tonk — Official Community Website
## 📖 About The Project

This is the official website for **Bairwa Mahasabha Tonk**, a grassroots community organisation based in Tonk, Rajasthan, India. The organisation is dedicated to the empowerment, education, and social upliftment of the Bairwa community — working tirelessly to ensure that no member of the community is left behind due to a lack of resources or opportunity.

The website serves as a digital home for the community — providing information about the organisation's mission, leadership, facilities, and allowing community members to register their interest in joining.

🔗 **Live Site**: [https://bairwa-mahasabha-3637f7.netlify.app/]

---

## ✨ Features

- **Hero Section** — Bold, animated landing with the organisation's name and tagline
- **About Section** — Organisation mission, core pillars, and vision statement
- **Leadership Section** — Showcase of the organisation's three key leaders with photos and titles
- **Member Directory Download** — One-click download of the complete member list (PDF)
- **Join Us Form** — Community members can submit their name and phone number to request membership
- **Contact Section** — Phone number and email for direct communication
- **Fully Responsive** — Works beautifully on mobile, tablet, and desktop
- **Smooth Animations** — Fade-in scroll animations and micro-interactions throughout

---

## 🏛️ About Bairwa Mahasabha Tonk

The Bairwa community has shown incredible resilience across generations. Bairwa Mahasabha Tonk was founded to transform that resilience into prosperity and self-reliance through three core pillars:

| Pillar | Description |
|---|---|
| 📚 **Education** | The Bairwa Community Library provides a quiet, resource-rich space for students preparing for competitive exams |
| 🏠 **Dharamshala** | A community sanctuary for shelter, social functions, and strengthening bonds of brotherhood |
| ✊ **Social Upliftment** | A platform for the underprivileged — driving economic stability, social dignity, and political awareness |

---

## 🛠️ Built With

- **HTML5** — Semantic, accessible markup
- **CSS3** — Custom properties, animations, responsive grid & flexbox layouts
- **Vanilla JavaScript** — Scroll animations, mobile menu, form handling
- **Google Fonts** — Tiro Devanagari Hindi + DM Sans
- **Netlify** — Hosting and form submissions
- **Google Apps Script** — Backend for storing membership requests in Google Sheets

---

## 🚀 Getting Started

### To run locally:

1. Clone the repository
```bash
git clone https://github.com/mohit-15-raj/bairwa-mahasabha-tonk.git
```

2. Open `index.html` in your browser — no build step or dependencies needed.

### Folder Structure

```
📁 bairwa-mahasabha-tonk/
  ├── index.html          # Main website file
  ├── 📁 photos/          # Leader profile photos
  │     ├── leader1.jpeg
  │     ├── leader2.jpeg
  │     └── leader3.jpeg
  ├── 📁 members/         # Member directory
  │     └── member-list.pdf
  └── README.md
```

---

## ⚙️ Configuration

### Connecting the Join Form to Google Sheets

1. Create a Google Sheet with columns: `Name | Phone | Date`
2. Go to **Extensions → Apps Script** and paste:

```javascript
function doPost(e) {
  const sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  const data = JSON.parse(e.postData.contents);
  sheet.appendRow([data.name, data.phone, data.date]);
  return ContentService.createTextOutput('OK');
}
```

3. Deploy as a **Web App** (access: Anyone)
4. Copy the deployment URL and paste it into `index.html`:

```javascript
const SCRIPT_URL = 'YOUR_GOOGLE_APPS_SCRIPT_URL_HERE';
```

### Updating Leader Photos & Names

In `index.html`, find the Leaders section and replace:
- `leader1.jpg / leader2.jpg / leader3.jpg` with actual photo filenames
- Placeholder names with actual leader names

### Updating the Member List PDF

Replace `members/member-list.pdf` with an updated PDF — keep the filename the same and redeploy to Netlify.

---

## 📦 Deployment

The site is deployed on **Netlify** via drag-and-drop:

1. Make your changes locally
2. Drag the project folder onto your Netlify site dashboard
3. The live site updates automatically — same URL, no downtime

---

## 🤝 Contributing

This project was built for the Bairwa community of Tonk, Rajasthan. If you'd like to suggest improvements or report issues, feel free to open an Issue or Pull Request.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙏 Acknowledgements

- The entire **Bairwa community of Tonk, Rajasthan** for their resilience and inspiration
- Dr. B.R. Ambedkar — *"Educate, Agitate, Organize."*

---

<p align="center">
  Made with ❤️ for the Bairwa Community · Tonk, Rajasthan, India
</p>
