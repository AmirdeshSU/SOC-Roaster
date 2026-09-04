# soc-roster
SOC Shift Roster Viewer
# 🛡️ SOC Shift Roster Viewer

A modern, feature-rich web application for managing and visualizing Security Operations Center (SOC) shift schedules. Built with vanilla JavaScript and designed for GitHub Pages deployment.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

---

## 🌟 Features

### 📅 **Automatic Roster Loading**
- Automatically fetches roster files from the repository
- Supports month-by-month navigation with Previous/Next buttons
- Loads current month by default
- Smart error handling with fallback to manual upload

### 📊 **Advanced Analytics**
- **Overall Statistics**: Total employees, shifts, averages, days off
- **Individual Statistics**: Personal shift breakdowns with percentages
- **Interactive Pie Charts**: Visual shift distribution for each employee
- **Consecutive Days Tracking**: Monitor workload and prevent burnout

### 🎨 **Modern UI/UX**
- **Dual Theme Support**: Beautiful dark and light modes
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile
- **Smooth Animations**: Loading states, transitions, and hover effects
- **Color-Coded Calendar**: Easy visual identification of shift types
- **Day-Off Highlighting**: Green background for individual days off

### 👥 **Employee Management**
- Filter view by individual employees
- Click employee cards to focus on their schedule
- Download individual or team-wide Excel reports
- Track shift distribution and workload balance

### 📥 **Flexible Data Input**
- **Repository Loading**: Automatically fetches from `/rosters/` folder
- **Manual Upload**: Drag-and-drop Excel files as backup
- **Month/Year Modal**: Beautiful date picker (no browser prompts!)
- **Multiple Format Support**: .xlsx and .xls files

### 📤 **Export Options**
- Download full roster as Excel
- Download individual employee schedules with summary sheets
- Formatted Excel output matching original structure
- Percentage calculations included

### 🔍 **Interactive Calendar**
- Click any day to see detailed shift assignments
- Modal popups with organized shift information
- Filter calendar by employee selection
- Visual indicators for holidays and days off

---

## 🚀 Quick Start

### **1. Set Up Repository**

```bash
# Create a new repository on GitHub named 'soc-roster'
# Clone it to your local machine
git clone https://github.com/AmirdeshSU/SOC-Roaster.git
cd soc-roster
```

### **2. Add Files**

```
soc-roster/
├── index.html          # Main application file
├── README.md           # This file
└── rosters/
    ├── 2026-01.xlsx   # January 2026
    ├── 2026-02.xlsx   # February 2026
    └── ...            # More months
```

### **3. Enable GitHub Pages**

1. Go to repository **Settings** → **Pages**
2. Under "Build and deployment":
   - **Source**: Deploy from a branch
   - **Branch**: main
   - **Folder**: / (root)
3. Click **Save**
4. Wait 1-2 minutes for deployment
5. Visit: `https://AmirdeshSU.github.io/soc-roster/`

---

## 📁 File Naming Convention

Roster files **must** follow this exact format:

```
YYYY-MM.xlsx
```

### Examples:
- ✅ `2026-01.xlsx` (January 2026)
- ✅ `2026-02.xlsx` (February 2026)
- ✅ `2026-12.xlsx` (December 2026)
- ❌ `Jan-2026.xlsx` (Wrong format)
- ❌ `2026-1.xlsx` (Missing leading zero)
- ❌ `January_2026.xlsx` (Wrong format)

---

## 📊 Excel File Structure

Your Excel files should have the following columns:

| Column | Description | Example |
|--------|-------------|---------|
| A | Date | 1/1/2026 |
| B | Day | Monday |
| C | Morning Shift (6 AM - 3 PM) | John, Sarah |
| D | Afternoon Shift (2 PM - 11 PM) | Mike, Lisa |
| E | Night Shift (10 PM - 7 AM) | David |
| F | Week Off | Emma, Tom |

**Note**: First row should be headers. Employee names can be comma-separated or on new lines.

---

## 🎯 Usage Guide

### **Viewing Rosters**

1. **Open the application** - Site loads current month automatically
2. **Navigate months** - Use Previous/Next buttons
3. **Filter by employee** - Select from dropdown
4. **Click days** - View detailed shift assignments
5. **Download** - Export full or individual schedules

### **Uploading New Rosters**

#### **Option A: Add to Repository (Recommended)**

1. Go to your GitHub repository
2. Navigate to `/rosters/` folder
3. Click **Add file** → **Upload files**
4. Drop your `YYYY-MM.xlsx` file(s)
5. Click **Commit changes**
6. Changes live in ~30 seconds!

#### **Option B: Manual Upload (Temporary)**

1. If roster file doesn't exist, upload section appears
2. Drag and drop or click to select Excel file
3. Beautiful modal appears for month/year selection
4. Click **Confirm**
5. Roster displays (not saved to repository)

---

## 🎨 Features Breakdown

### **Calendar View**
- 7-column grid layout (Sun-Sat)
- Color-coded shifts:
  - 🌅 **Morning**: Yellow/Gold
  - 🌤️ **Afternoon**: Blue
  - 🌙 **Night**: Purple
  - 🏖️ **Day Off**: Green
- Hover effects for interactivity
- Click to expand day details

### **Employee Statistics**
- Total shifts worked
- Shift type breakdown (Morning/Afternoon/Night)
- Days off count
- Maximum consecutive work days
- Visual indicators for workload

### **Pie Chart Analytics**
- Click "📊 Show Pie Chart" when employee selected
- Beautiful modal with Chart.js visualization
- Percentage distribution of shift types
- Color-coded segments matching shift colors
- Responsive and theme-aware

### **Theme Switching**
- **Dark Mode** (Default): Easy on eyes, perfect for SOC environment
- **Light Mode**: Clean and professional
- Theme preference saved in browser
- Chart colors adapt automatically

### **Download Options**
- **Download All**: Full month roster with all employees
- **Download Individual**: 2-sheet Excel file
  - **Summary Sheet**: Stats, percentages, totals
  - **Roster Sheet**: Personal schedule for the month

---

## 🛠️ Technical Details

### **Built With**
- **HTML5** - Structure
- **CSS3** - Styling with CSS Variables for theming
- **Vanilla JavaScript** - No frameworks, pure JS
- **SheetJS (XLSX.js)** - Excel file parsing
- **Chart.js** - Pie chart visualizations
- **Google Fonts** - DM Sans & JetBrains Mono

### **Browser Support**
- ✅ Chrome/Edge (v90+)
- ✅ Firefox (v88+)
- ✅ Safari (v14+)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

### **Performance**
- **Lightweight**: Single HTML file (~100KB)
- **Fast Loading**: Minimal external dependencies
- **Client-Side Only**: No server required
- **Caching**: Browser caches assets automatically

### **No Backend Required**
- Fully static application
- Runs entirely in browser
- Perfect for GitHub Pages
- No database needed

---

## 📱 Mobile Optimization

- Responsive grid layouts
- Touch-friendly tap targets
- Swipe-friendly navigation
- Collapsible sections
- Optimized font sizes
- Mobile-first design approach

---

## 🔒 Privacy & Security

- **No Data Collection**: All processing happens in browser
- **No Analytics**: No tracking scripts
- **Local Storage Only**: Theme preference saved locally
- **No External APIs**: Except CDN for libraries
- **Public Data**: Designed for team-shared schedules

---

## 🔄 Monthly Update Workflow

### **Standard Process:**

1. **Export** roster from your SOC management tool (Zoho, Excel, etc.)
2. **Rename** file to `YYYY-MM.xlsx` format
3. **Navigate** to GitHub repository → `rosters/` folder
4. **Upload** file via drag-and-drop
5. **Commit** changes
6. **Done!** Live in 30 seconds

### **Bulk Upload:**

Upload multiple months at once:
```
rosters/
├── 2026-01.xlsx
├── 2026-02.xlsx
├── 2026-03.xlsx
├── 2026-04.xlsx
├── 2026-05.xlsx
└── 2026-06.xlsx
```

All files process in one commit!

---

## 🎓 Tips & Best Practices

### **For Administrators:**
- Upload 3-6 months in advance
- Keep consistent file naming
- Archive old months (move to `/archive/` folder)
- Test new uploads with Previous/Next buttons
- Share repository URL with team

### **For Team Members:**
- Bookmark the site URL
- Use employee filter to see personal schedule
- Download individual Excel for offline access
- Check "Max Consecutive Days" to avoid burnout
- Use calendar click for day details

### **For Developers:**
- Repository structure is simple and maintainable
- All code in single `index.html` for easy deployment
- CSS variables make theming easy
- Well-commented JavaScript
- No build process required

---

## 🐛 Troubleshooting

### **Roster Not Loading**
- ✅ Check file naming: `YYYY-MM.xlsx` (exact format)
- ✅ Verify file is in `/rosters/` folder
- ✅ Check month/year matches navigation
- ✅ Hard refresh browser: `Ctrl+Shift+R`

### **Upload Not Working**
- ✅ Check file format (.xlsx or .xls)
- ✅ Verify Excel structure matches template
- ✅ Try different browser
- ✅ Check browser console (F12) for errors

### **Calendar Shows Wrong Dates**
- ✅ Check date column in Excel (Column A)
- ✅ Verify month/year in upload modal
- ✅ Ensure dates are sequential

### **Charts Not Displaying**
- ✅ Check internet connection (Chart.js loads from CDN)
- ✅ Disable ad blockers temporarily
- ✅ Try different browser

### **Site Not Updating**
- ✅ Wait 2-3 minutes after commit
- ✅ Check Actions tab for build status
- ✅ Hard refresh: `Ctrl+Shift+R` or `Cmd+Shift+R`
- ✅ Try incognito/private mode

---

## 📖 Documentation

### **Additional Resources:**
- See `GITHUB_SETUP_GUIDE.md` for detailed setup instructions
- Excel template available in `/templates/` folder (if added)
- Color scheme reference in CSS variables section

### **Algorithm Philosophy:**
Based on "Flexible Fairness" principles:
- Coverage-based flexible staffing
- Balanced workload distribution
- Sustainable work patterns
- Minimal multi-shift burden
- Respects employee constraints

---

## 🤝 Contributing

This is designed as a turnkey solution, but improvements welcome:

1. Fork the repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

### **Ideas for Contribution:**
- Additional export formats (PDF, CSV)
- Print-optimized view
- Email notification integration
- Shift swap request feature
- Mobile app version
- Multi-language support

---

## 📄 License

This project is licensed under the MIT License - see below for details:

```
MIT License

Copyright (c) 2026 SOC Shift Roster Viewer

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Acknowledgments

- **SheetJS** - Excel file processing
- **Chart.js** - Beautiful charts
- **Google Fonts** - Typography
- **GitHub Pages** - Free hosting
- **SOC Teams Worldwide** - Inspiration and use case

---

## 📞 Support

### **Having Issues?**
1. Check Troubleshooting section above
2. Review GITHUB_SETUP_GUIDE.md
3. Open an issue on GitHub
4. Check browser console for errors

### **Feature Requests?**
Open an issue with:
- Clear description of feature
- Use case/benefit
- Example or mockup (if applicable)

---

## 🚀 Roadmap

### **Potential Future Enhancements:**
- [ ] PDF export with formatting
- [ ] Dark/Light/Auto theme modes
- [ ] Calendar sync (Google, Outlook)
- [ ] Shift swap management
- [ ] Mobile PWA version
- [ ] Multi-team support
- [ ] Historical analytics
- [ ] Slack/Teams integration
- [ ] Custom shift types
- [ ] Overtime calculations

---

## 📊 Stats

![GitHub repo size](https://img.shields.io/github/repo-size/AmirdeshSU/SOC-Roaster)
![GitHub stars](https://img.shields.io/github/stars/AmirdeshSU/SOC-Roaster?style=social)
![GitHub forks](https://img.shields.io/github/forks/AmirdeshSU/SOC-Roaster?style=social)

---

## 📝 Changelog

### **Version 1.0.0** (2026-01-02)
- ✨ Initial release
- 🎨 Dark/Light theme support
- 📊 Pie chart analytics
- 📥 Auto-load from repository
- 📤 Manual upload fallback
- 🗓️ Month navigation
- 👤 Individual filtering
- 📈 Advanced statistics
- 🎯 Beautiful UI/UX
- 📱 Mobile responsive

---

<div align="center">

**Built with ❤️ for SOC Teams**

[Live Demo](https://AmirdeshSU.github.io/soc-roster/) • [Report Bug](https://github.com/AmirdeshSU/SOC-Roaster/issues) • [Request Feature](https://github.com/AmirdeshSU/SOC-Roaster/issues)

⭐ **Star this repo if it helps your team!** ⭐

</div>
