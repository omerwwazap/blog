# Local Development Guide

This guide will help you run the blog locally for testing and development purposes.

## Prerequisites

Before you begin, make sure you have the following installed:

1. **Ruby** (version 2.5 or higher)
   - Download from: https://rubyinstaller.org/ (for Windows)
   - Verify installation: `ruby --version`

2. **Bundler** (Ruby package manager)
   - Install with: `gem install bundler`
   - Verify installation: `bundle --version`

3. **Git** (optional, for version control)
   - Download from: https://git-scm.com/

## Step-by-Step Setup

### Step 1: Navigate to the Project Directory

Open your terminal (PowerShell or Command Prompt) and navigate to the blog directory:

```bash
cd C:\Users\leven\Desktop\Github-omerwwazap\blog
```

Or navigate to wherever you have cloned the repository.

### Step 2: Install Dependencies

Install all required Ruby gems and dependencies:

```bash
bundle install
```

This command will:
- Read the `Gemfile` in your project
- Download and install all necessary gems
- Create a `Gemfile.lock` file to lock dependency versions

**Expected output:** You should see a message like "Bundle complete! X Gemfile dependencies, Y gems now installed."

### Step 3: Start the Local Server

Run the Jekyll development server with live reload:

```bash
bundle exec jekyll serve --livereload
```

**What this does:**
- Builds your Jekyll site
- Starts a local web server
- Enables live reload (automatically refreshes browser when files change)
- Watches for file changes

**Expected output:**
```
Configuration file: C:/Users/leven/Desktop/Github-omerwwazap/blog/_config.yml
            Source: C:/Users/leven/Desktop/Github-omerwwazap/blog
       Destination: C:/Users/leven/Desktop/Github-omerwwazap/blog/_site
      Generating... 
                    done in 12.875 seconds.
 Auto-regeneration: enabled
LiveReload address: http://127.0.0.1:35729
    Server address: http://127.0.0.1:4000/blog/
  Server running... press ctrl-c to stop.
```

### Step 4: View Your Blog

Open your web browser and navigate to:

```
http://127.0.0.1:4000/blog/
```

or

```
http://localhost:4000/blog/
```

**Note:** The `/blog` part is important because it's defined in your `_config.yml` as the `baseurl`.

### Step 5: Make Changes and Test

The server is now running with live reload enabled. Any changes you make will automatically refresh in your browser!

## Working with Posts

### Creating a New Post

1. Create a new file in the `_posts` directory
2. Name it using the format: `YYYY-MM-DD-title-of-post.md`
   - Example: `2025-10-27-my-new-post.md`

3. Add front matter at the top of the file:

```yaml
---
title: My New Post Title
date: 2025-10-27 14:30:00 +0300
categories: [cyber-security, osint]
tags: [security, analysis, tools]
---

Your content starts here...
```

4. Save the file and the browser will automatically refresh showing your new post!

### Working with Drafts

1. Create files in the `_drafts` directory (no date needed in filename)
   - Example: `my-draft-post.md`

2. To view drafts locally, run:

```bash
bundle exec jekyll serve --livereload --drafts
```

3. Drafts won't be published when you deploy to production

### Post Front Matter Fields

Here are the common fields you can use in your post's front matter:

```yaml
---
title: Post Title                              # Required
date: YYYY-MM-DD HH:MM:SS +TIMEZONE           # Required
categories: [category1, category2]             # Optional
tags: [tag1, tag2, tag3]                      # Optional
image:                                         # Optional - featured image
  path: /images/2025/my-image.png
  alt: Image description
toc: true                                      # Optional - Table of Contents (default: true)
comments: true                                 # Optional - Enable comments (default: true)
pin: true                                      # Optional - Pin post to top
---
```

## Common Commands

### Basic Server Start
```bash
bundle exec jekyll serve
```

### With Live Reload (Recommended)
```bash
bundle exec jekyll serve --livereload
```

### With Drafts
```bash
bundle exec jekyll serve --livereload --drafts
```

### With Incremental Build (Faster Rebuilds)
```bash
bundle exec jekyll serve --livereload --incremental
```

### Build Only (No Server)
```bash
bundle exec jekyll build
```

### Clean Build Files
```bash
bundle exec jekyll clean
```

## Stopping the Server

To stop the Jekyll server:
- Press `Ctrl+C` in the terminal where the server is running
- Confirm with `Y` if prompted

## Troubleshooting

### Issue: Port Already in Use

If you see an error like "Address already in use", the port 4000 is occupied:

**Solution:** Use a different port:
```bash
bundle exec jekyll serve --livereload --port 4001
```

Then access your site at: `http://127.0.0.1:4001/blog/`

### Issue: Changes Not Showing Up

1. **Hard refresh your browser:** Press `Ctrl+F5` (Windows) or `Cmd+Shift+R` (Mac)
2. **Restart the server:** Stop with `Ctrl+C` and start again
3. **Clear the cache:** Run `bundle exec jekyll clean` then restart

### Issue: Config Changes Not Applied

**Solution:** The `_config.yml` file requires a server restart to apply changes:
1. Stop the server (`Ctrl+C`)
2. Start it again (`bundle exec jekyll serve --livereload`)

### Issue: Bundle Install Fails

**Solution:** Update bundler and try again:
```bash
gem update bundler
bundle install
```

### Issue: Ruby Version Mismatch

**Solution:** Check your Ruby version:
```bash
ruby --version
```

Make sure it's 2.5 or higher. Update Ruby if needed.

## Project Structure

```
blog/
├── _config.yml           # Site configuration
├── _posts/               # Published blog posts
├── _drafts/              # Draft posts (not published)
├── _tabs/                # Static pages (CV, Projects, etc.)
├── _data/                # Data files (contact, share settings)
├── _site/                # Generated site (don't edit directly)
├── assets/               # Images, CSS, JavaScript
├── images/               # Post images organized by folder
├── Gemfile               # Ruby dependencies
└── Gemfile.lock          # Locked dependency versions
```

## Tips for Local Development

1. **Keep the server running** while you work on multiple posts
2. **Use drafts** for work-in-progress posts
3. **Test on different screen sizes** using browser dev tools
4. **Check for broken links** before deploying
5. **Verify images load correctly** from the `images/` directory
6. **Test dark/light mode** if your theme supports it

## Before Deploying

Before pushing changes to production, make sure to:

1. ✅ Test all new posts locally
2. ✅ Check for spelling and grammar errors
3. ✅ Verify all images load correctly
4. ✅ Test internal and external links
5. ✅ Review the post in both light and dark modes
6. ✅ Check mobile responsiveness
7. ✅ Move drafts from `_drafts/` to `_posts/` with proper date

## Additional Resources

- **Jekyll Documentation:** https://jekyllrb.com/docs/
- **Chirpy Theme Documentation:** https://github.com/cotes2020/jekyll-theme-chirpy
- **Markdown Guide:** https://www.markdownguide.org/
- **Front Matter Reference:** https://jekyllrb.com/docs/front-matter/

## Getting Help

If you encounter issues not covered in this guide:

1. Check the Jekyll documentation
2. Review the Chirpy theme issues on GitHub
3. Search for similar problems online
4. Check the build logs for error messages

---

**Happy blogging! 🚀**

