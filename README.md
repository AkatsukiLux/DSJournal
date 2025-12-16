# DSJournal - Data Science Journal

My collection of data-driven project management insights, with a focus on the construction industry.

## About

This blog explores the intersection of data analytics and project management in construction. Topics include API integrations, business intelligence tools, text analytics, and practical solutions for construction project challenges.

## Tech Stack

- **Jekyll**: Static site generator
- **Theme**: Minima
- **Markdown**: kramdown
- **Hosting**: GitHub Pages

## Local Development

### Prerequisites

- Ruby (version 2.5 or higher)
- Bundler gem
- Git

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/AtsutoB/DSJournal.git
   cd DSJournal
   ```

2. **Install dependencies**
   ```bash
   bundle install
   ```

3. **Run the local server**
   ```bash
   bundle exec jekyll serve
   ```

4. **View the site**
   Open your browser and navigate to `http://localhost:4000`

### Development Commands

- **Build site**: `bundle exec jekyll build`
- **Serve locally**: `bundle exec jekyll serve`
- **Serve with drafts**: `bundle exec jekyll serve --drafts`
- **Clean build files**: `bundle exec jekyll clean`

## Project Structure

```
DSJournal/
├── _posts/              # Blog posts (YYYY-MM-DD-title.md format)
├── assets/              # Images, CSS, JS files
│   └── photos/          # Blog post images
├── _config.yml          # Jekyll configuration
├── about.md             # About page
├── Gemfile              # Ruby dependencies
├── .gitignore           # Git ignore rules
└── README.md            # This file
```

## Writing Posts

Create new posts in the `_posts/` directory with the following format:

```markdown
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD
categories: [category1, category2]
tags: [tag1, tag2, tag3]
---

Your content here...
```

### Post Naming Convention

Files should be named: `YYYY-MM-DD-post-title.md`

Example: `2018-07-19-TextAnalytics.md`

## Topics Covered

- **Fieldview API Integration**: Practical guides for construction management systems
- **Excel & Power BI**: Data integration and visualization tutorials
- **Text Analytics**: NLP applications for industry insights
- **Data-Driven Project Management**: Analytics for construction projects

## Contributing

This is a personal blog, but if you spot any issues or have suggestions, feel free to:

1. Open an issue
2. Submit a pull request
3. Contact me via email or social media

## Contact

- **Author**: AtsutoB
- **Email**: atsutobriggs@gmail.com
- **Twitter**: [@atsutobriggs](https://twitter.com/atsutobriggs)
- **GitHub**: [AtsutoB](https://github.com/AtsutoB)

## License

Content is available for personal and educational use. Please provide attribution when sharing or referencing blog content.

## Acknowledgments

Built with [Jekyll](https://jekyllrb.com/) and hosted on [GitHub Pages](https://pages.github.com/).
