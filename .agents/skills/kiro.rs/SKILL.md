```markdown
# kiro.rs Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `kiro.rs` Rust codebase. It covers file organization, code style, commit message standards, and testing patterns. By following these guidelines, contributors can maintain consistency and quality across the project.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myModule.rs`, `userProfile.rs`

### Import Style
- Use **relative imports** within the codebase.
  - Example:
    ```rust
    mod utils;
    use crate::utils::parseData;
    ```

### Export Style
- Use **named exports** for modules and functions.
  - Example:
    ```rust
    pub fn processData() { /* ... */ }
    ```

### Commit Messages
- Follow the **conventional commit** format.
- Use the `feat` prefix for new features.
- Keep commit messages concise (average: ~47 characters).
  - Example:
    ```
    feat: add user authentication middleware
    ```

## Workflows

### Feature Development
**Trigger:** When adding a new feature to the codebase  
**Command:** `/feature-development`

1. Create a new branch for your feature.
2. Implement the feature using camelCase file naming and relative imports.
3. Write or update tests in `*.test.*` files.
4. Commit changes using the `feat` prefix and a concise message.
5. Open a pull request for review.

### Code Testing
**Trigger:** When verifying code correctness  
**Command:** `/run-tests`

1. Identify or create test files matching the `*.test.*` pattern.
2. Run tests using the project's preferred Rust testing command (e.g., `cargo test`).
3. Review test results and fix any failures.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern.
  - Example: `parser.test.rs`
- Testing framework is not explicitly defined; use standard Rust test modules.
  - Example:
    ```rust
    #[cfg(test)]
    mod tests {
        use super::*;

        #[test]
        fn test_parse_data() {
            assert_eq!(parseData("input"), "expected");
        }
    }
    ```

## Commands
| Command              | Purpose                                   |
|----------------------|-------------------------------------------|
| /feature-development | Start a new feature workflow              |
| /run-tests           | Run all tests in the codebase             |
```
