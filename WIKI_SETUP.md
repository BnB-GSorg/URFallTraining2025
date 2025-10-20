# Wiki Setup Guide

This document explains how to set up the GitHub Wiki using the sample wiki pages provided in the `/wiki` directory.

## Overview

This repository includes pre-written wiki pages that provide comprehensive documentation for the URFallTraining2025 project. These pages are located in the `/wiki` directory and need to be manually added to GitHub's Wiki feature.

## Wiki Pages Included

The following wiki pages are available:

1. **Home.md** - Main landing page with project overview
2. **FAQ.md** - Frequently asked questions
3. **Installation.md** - Installation and setup instructions
4. **Project-Structure.md** - Repository organization details

## How to Set Up the GitHub Wiki

### Method 1: Using GitHub Web Interface (Easiest)

1. **Enable Wiki**
   - Go to https://github.com/BnB-GSorg/URFallTraining2025
   - Click on "Settings" tab
   - Scroll down to "Features" section
   - Check the "Wikis" checkbox if not already enabled

2. **Access the Wiki**
   - Click on the "Wiki" tab at the top of the repository
   - Click "Create the first page" button

3. **Create Home Page**
   - Open `/wiki/Home.md` from this repository
   - Copy all the content
   - Paste it into the GitHub wiki editor
   - Save the page (it will automatically be named "Home")

4. **Create Additional Pages**
   - Click "New Page" button
   - For FAQ page:
     - Title: `FAQ`
     - Copy content from `/wiki/FAQ.md`
     - Paste and save
   - For Installation page:
     - Title: `Installation`
     - Copy content from `/wiki/Installation.md`
     - Paste and save
   - For Project Structure page:
     - Title: `Project-Structure`
     - Copy content from `/wiki/Project-Structure.md`
     - Paste and save

### Method 2: Using Git (Advanced)

GitHub wikis are actually Git repositories themselves. You can clone and push to them:

1. **Clone the Wiki Repository**
   ```bash
   git clone https://github.com/BnB-GSorg/URFallTraining2025.wiki.git
   cd URFallTraining2025.wiki
   ```

2. **Copy Wiki Files**
   ```bash
   cp ../URFallTraining2025/wiki/*.md .
   ```

3. **Commit and Push**
   ```bash
   git add .
   git commit -m "Add initial wiki pages"
   git push origin master
   ```

Note: The wiki repository uses `master` branch by default, not `main`.

## Customization Tips

After setting up the wiki, you may want to customize it:

### Update Project-Specific Information

- Replace placeholder text with actual project details
- Add links to actual resources and tools used
- Include contact information for project maintainers
- Add screenshots and diagrams

### Add More Pages

Consider adding these additional pages as your project grows:

- **Tutorials** - Step-by-step guides
- **API Documentation** - If you have code with APIs
- **Design Philosophy** - Explain design decisions
- **Roadmap** - Future plans and milestones
- **Changelog** - Track major changes
- **Troubleshooting** - Common issues and solutions
- **Resources** - External links and references
- **Team** - Contributors and maintainers

### Link Between Pages

Use relative links to connect pages:
```markdown
See the [Installation Guide](Installation) for setup instructions.
Check out our [FAQ](FAQ) for common questions.
```

### Add Images

You can upload images to the wiki:

1. Edit a wiki page
2. Drag and drop an image into the editor
3. GitHub will upload it and generate the markdown syntax
4. Or use: `![Alt text](image-url)`

### Create a Sidebar

Add a file named `_Sidebar.md` to create a navigation sidebar:

```markdown
### Navigation

- [Home](Home)
- [Installation](Installation)
- [FAQ](FAQ)
- [Project Structure](Project-Structure)

### Quick Links

- [Issues](https://github.com/BnB-GSorg/URFallTraining2025/issues)
- [Pull Requests](https://github.com/BnB-GSorg/URFallTraining2025/pulls)
```

### Create a Footer

Add a file named `_Footer.md` to add a footer to all pages:

```markdown
---
URFallTraining2025 | [Report an Issue](https://github.com/BnB-GSorg/URFallTraining2025/issues) | Licensed under CC0 1.0
```

## Maintenance

Keep your wiki up to date:

- **Regular Reviews**: Review wiki content quarterly
- **Update with Changes**: When repository structure changes, update Project-Structure page
- **Monitor Questions**: Add common questions to FAQ
- **Fix Broken Links**: Check and update links regularly
- **Version Information**: Update "Last updated" dates

## Wiki Best Practices

1. **Keep it Simple**: Write clear, concise content
2. **Use Headers**: Organize content with proper heading hierarchy
3. **Add Links**: Link to relevant pages and external resources
4. **Include Examples**: Show code examples and use cases
5. **Stay Consistent**: Maintain consistent formatting and style
6. **Test Links**: Verify all links work correctly
7. **Welcome Contributions**: Encourage others to improve wiki

## Troubleshooting

### Wiki Tab Not Visible

- Check repository settings to ensure Wikis are enabled
- Refresh the page
- Check if you have permission to view the wiki

### Can't Edit Wiki

- Ensure you have write access to the repository
- Check if the wiki is restricted to collaborators only
- Contact repository administrators

### Formatting Issues

- Preview your changes before saving
- Check markdown syntax
- Use GitHub's markdown guide: https://guides.github.com/features/mastering-markdown/

## Getting Help

If you need help setting up the wiki:

1. Check GitHub's wiki documentation: https://docs.github.com/en/communities/documenting-your-project-with-wikis
2. Open an issue in the repository
3. Ask in discussions (if enabled)

## Additional Resources

- [GitHub Markdown Guide](https://guides.github.com/features/mastering-markdown/)
- [GitHub Wiki Documentation](https://docs.github.com/en/communities/documenting-your-project-with-wikis)
- [Markdown Cheatsheet](https://www.markdownguide.org/cheat-sheet/)

---

*This guide is part of the URFallTraining2025 repository documentation.*
