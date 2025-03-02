# My AI Agent Prompts
My AI prompts to use with the agent of Cursor, Windsurf, etc

## Documentation

### Generate high level documentation for a project:

#### General projects
```
# Task Overview

You are an expert in code analysis and project documentation. Your task is to document the structure and functionality of the project's source files by using the macOS terminal and updating the `@FOLDER_STRUCTURE.md` file accordingly.

## Instructions

1. **List Files in the `src` Directory:**
   - Execute a terminal command on macOS to recursively traverse the `src` directory and list all file paths.
   - Capture the output of this command, which should contain the path of each file.

2. **Update the Folder Structure:**
   - Open or create the `@FOLDER_STRUCTURE.md` file.
   - Add all the file paths obtained in step 1 to this document, using a clear and readable format (e.g., lists or tables).

3. **Detailed Analysis and Documentation of Each File:**
   - Iterate over each file listed in `@FOLDER_STRUCTURE.md` in the order they appear.
   - For each file, perform the following steps:
     - **Read the File:** Open and read the content of the file.
     - **Explain the File:** Write a clear and concise explanation of the file's functionality and purpose.
     - **Document the Explanation:** Insert this explanation into `@FOLDER_STRUCTURE.md` alongside the corresponding file path.
     - **Iterative Confirmation:** After documenting each file, pause and ask for user confirmation to ensure that the explanation meets their expectations before proceeding to the next file.

4. **Iterative Process and Validation:**
   - Ensure that you stop after each file for confirmation that the explanation is satisfactory.
   - If the user requests adjustments or improvements, make them before moving on to the next file.

## Additional Notes
- Maintain a methodical and organized approach, ensuring each step is completed correctly before advancing.
- If any uncertainties arise regarding the content or required format, request clarification from the user.
```

#### NodeJS projects
```
**Objective:**  
Analyze the entire codebase of a software project to create a comprehensive, modular, and developer-friendly set of documentation files within a `/docs` folder at the root of the repository.

---

## Instructions

### 1. Codebase Analysis

- **Scope of Analysis:**  
  - Review all aspects of the project including:
    - `package.json` scripts
    - Project dependencies
    - Existing README files and documentation
    - The current folder structure (use CLI commands for an accurate and detailed view)

- **Purpose:**  
  - Understand the project’s overall structure, architecture, and functionalities.

---

### 2. Documentation Structure

Generate separate markdown files within the `/docs` folder. Each file should be self-contained, focusing on a specific aspect of the project. The files to be created are:

1. **`/docs/README.md`**  
   - Provide a high-level project overview.
   - Describe the project’s purpose.
   - Include a quick start guide for developers.

2. **`/docs/folder-structure.md`**  
   - Detail the project’s directory structure.
   - Explain the purpose of each key file and folder.
   - Base your explanation on the output of CLI commands used to explore the folder structure.

3. **`/docs/architecture.md`**  
   - Outline the system architecture and the interaction between services.
   - Provide high-level design details.
   - Include diagrams in **Mermaid** format using **Material Design colors** and high-contrast text to illustrate important components and their relationships.

4. **`/docs/development-guide.md`**  
   - Detail the setup instructions for developers.
   - List key dependencies and important scripts.
   - Explain how to configure and run the development environment.

5. **`/docs/operations.md`**  
   - Document the deployment process, including CI/CD pipelines.
   - Explain configuration options and operational guidelines.

6. **`/docs/api-reference.md`**  
   - Provide details on API endpoints (if applicable).
   - Include request/response structures, authentication methods, and usage examples.

---

### 3. Iterative Generation and Validation

- **Step-by-Step Creation:**  
  - Generate each documentation file one by one.
  - After creating each file, present it for validation and confirmation.
  - Do not proceed to the next file until the current file has been reviewed and approved.

- **Clarification and Confirmation:**  
  - If any part of the instructions or content requires clarification, ask for further details before continuing.

---

### 4. Best Practices

- **Modularity:**  
  - Keep each documentation file focused on a single aspect of the project.
  
- **Separation of Concerns:**  
  - Avoid redundancy by ensuring each file covers distinct topics without overlap.

- **Accessibility:**  
  - Ensure all diagrams and documentation content follow industry best practices for clarity and accessibility.

- **Developer Onboarding:**  
  - Optimize the documentation for ease of understanding, quick onboarding, and maintainability.

---

**Final Check:**  
Before finalizing, ensure that every section is clear, accurate, and follows the structure above. Confirm with the user after each step to ensure that all documentation meets expectations.

---
```

## Git Management

### Generate commit messages

```md
Based on the latest changes discussed about "<CONTEXT>", please generate a commit message in English that follows the Conventional Commits format. The message should clearly and concisely summarize the modifications, including the appropriate commit type (e.g., feat, fix, docs, etc.) to reflect the changes accurately.
```
