# Documentation

This guide covers how to contribute to Voyager Verifier's documentation.

## Overview

Good documentation is crucial for project success. We welcome contributions that:

- Fix typos and grammatical errors
- Clarify confusing explanations
- Add missing information
- Improve code examples
- Update outdated content
- Add tutorials and guides

## Documentation Structure

Our documentation is organized as follows:

```
docs/
├── src/
│   ├── SUMMARY.md           # Table of contents
│   ├── introduction.md      # Getting started
│   ├── architecture/        # System design docs
│   ├── api/                 # API reference
│   ├── guides/              # How-to guides
│   └── contributing/        # Contribution guidelines
```

## Making Changes

### 1. Open an Issue First

Before making documentation changes, please open an issue to:

- Discuss significant restructuring or additions
- Get feedback on your proposed changes
- Ensure the changes align with documentation goals

For minor fixes (typos, formatting), you can skip this step.

### 2. Build Documentation Locally

We use [mdBook](https://rust-lang.github.io/mdBook/) for documentation.

Install mdBook:
```bash
cargo install mdbook
```

Build and serve locally:
```bash
cd docs
mdbook serve
```

Then open `http://localhost:3000` in your browser to preview changes.

### 3. Make Your Changes

Edit the Markdown files in `docs/src/`. As you save, mdBook will automatically rebuild and refresh your browser.

## Writing Guidelines

### Style and Tone

- **Clear and concise** - Use simple, direct language
- **Active voice** - "The verifier checks" instead of "The check is performed"
- **Present tense** - "The function returns" not "The function will return"
- **Second person** - Address the reader as "you"
- **Technical but accessible** - Explain concepts without oversimplifying

### Structure

- **Start with overview** - Begin each section with a summary
- **Progressive detail** - Go from simple to complex
- **Use headings** - Break content into scannable sections
- **Include examples** - Show concrete usage
- **Add context** - Explain the "why" not just the "how"

### Code Examples

- **Complete and runnable** - Examples should work as-is
- **Realistic** - Use meaningful variable names and scenarios
- **Commented** - Explain non-obvious parts
- **Tested** - Ensure examples actually work

Example format:
```rust
// Verify a Cairo contract on Starknet
use voyager_verifier::Verifier;

fn main() -> Result<(), Box<dyn std::error::Error>> {
    let verifier = Verifier::new("https://api.voyager.online");

    // Submit verification request
    let result = verifier.verify(
        "0x1234...",  // Contract address
        "path/to/source.cairo"
    )?;

    println!("Verification: {:?}", result);
    Ok(())
}
```

### Markdown Best Practices

- Use fenced code blocks with language hints: ` ```rust `
- Use relative links for internal pages: `[Guide](../guides/quickstart.md)`
- Add alt text to images: `![Architecture diagram](../images/arch.png)`
- Use tables for structured data
- Use admonitions for warnings/notes if supported

### API Documentation

When documenting APIs:

- **Function signature** - Show the full signature
- **Parameters** - List all parameters with types and descriptions
- **Return value** - Describe what is returned
- **Errors** - Document possible error conditions
- **Examples** - Provide usage examples
- **Related** - Link to related functions/types

## Common Documentation Tasks

### Adding a New Page

1. Create the Markdown file in the appropriate directory
2. Add it to `docs/src/SUMMARY.md` in the correct section
3. Link to it from related pages

### Updating API Documentation

1. Update the relevant Rust doc comments in source code
2. Update the corresponding API reference page if it exists
3. Update any examples that reference the changed API

### Adding Code Examples

1. Write the example code
2. Test that it compiles and runs correctly
3. Add explanatory comments
4. Include it in the documentation with context

### Fixing Broken Links

1. Use `mdbook build` to check for broken links
2. Update links to point to the correct location
3. Use relative paths for internal links

## Documentation Checklist

Before submitting your documentation changes:

- [ ] Spell check and grammar check completed
- [ ] Code examples tested and working
- [ ] Links verified (no broken links)
- [ ] Documentation builds without errors: `mdbook build`
- [ ] Preview looks correct: `mdbook serve`
- [ ] Changes reviewed in browser at `http://localhost:3000`
- [ ] SUMMARY.md updated if new pages added
- [ ] Related pages updated to cross-reference new content

## Review Process

1. Submit your PR referencing the related issue
2. Maintainers will review for:
   - Technical accuracy
   - Clarity and readability
   - Consistency with existing docs
   - Proper formatting and structure
3. Address any feedback
4. Once approved, your changes will be merged and published

## Style Reference

### Headings

```markdown
# Page Title (H1 - one per page)

## Major Section (H2)

### Subsection (H3)

#### Minor Section (H4)
```

### Emphasis

```markdown
**Bold** for emphasis and UI elements
*Italic* for introducing new terms
`code` for inline code and commands
```

### Lists

```markdown
- Unordered list item
- Another item
  - Nested item

1. Ordered list item
2. Second item
```

### Code Blocks

````markdown
```rust
// Rust code
fn main() {
    println!("Hello, world!");
}
```

```bash
# Shell commands
cargo build
```
````

### Links

```markdown
[Link text](https://example.com)
[Internal link](../other-page.md)
[Heading link](#heading-anchor)
```

## Questions?

If you have questions about documentation:

- Check existing documentation pages as examples
- Review the mdBook documentation
- Open an issue to discuss your plans
- Ask in your pull request

Thank you for helping improve Voyager Verifier's documentation!
