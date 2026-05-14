## System Dependencies

### libvips (required for image variants)

Active Storage uses libvips to resize and crop pet photos into thumbnails.

** With Homebrew:**
```bash
brew install vips
```


## Setup & Running

```bash
bundle install
bin/rails db:setup
bin/rails server
```


## Trix Sanitization Check

Action Text uses the Trix editor, which sanitizes all HTML input by default.

**Verification:** When `<script>alert(1)</script>` was pasted into the clinical notes rich text editor and saved, no alert fired on the appointment show page, and rich editor was working correctly. The script tag was stripped from the rendered HTML only safe, formatted content was displayed.