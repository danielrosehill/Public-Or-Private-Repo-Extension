# VS Code Extension Plan: GitHub Repository Visibility Notifier

## **Purpose**
The purpose of this VS Code extension is to notify users whether they are working in a GitHub repository whose remote is public or private. This will help developers quickly identify the visibility of their repositories while working within their development environment.

---

## **Scope of the First Version**
The initial version of the extension will:
- Cater to simple GitHub repositories with a single remote URL.
- Exclude support for repositories with submodules or multiple remotes.

---

## **Features**
1. **Repository Visibility Notification**
   - The extension will analyze the remote URL of the GitHub repository and determine if it is public or private.
   - A notification system will display this information prominently in the **status bar**.

2. **Visual Indicators**
   - The notification will include:
     - An icon to indicate visibility status (yellow for public, green for private).
     - A text label specifying whether the repository is *PUBLIC* or *PRIVATE*.
     - A clickable link to open the repository in a browser.

3. **Remote URL Conversion**
   - The remote URL will be converted into a browser-accessible format by removing the `.git` extension.

---

## **Notification Design**

### **Public Repository**
- **Icon**: Yellow circle
- **Text**: 
  - A globe icon next to the yellow circle.
  - The word *PUBLIC* in bold.
- **Link**: A clickable "Open Repo" link that redirects to the browser-accessible repository URL.

#### Example Layout:
| Icon | Text | Link |
|------|------|------|
| 🟡 🌐 | **PUBLIC** | [Open Repo](#) |

---

### **Private Repository**
- **Icon**: Green circle
- **Text**:
  - The word *PRIVATE* in ordinary white font (not bold).
- **Link**: A clickable "Open Repo" link that redirects to the browser-accessible repository URL.

#### Example Layout:
| Icon | Text | Link |
|------|------|------|
| 🟢 | PRIVATE | [Open Repo](#) |

---

## **Implementation Details**

1. **Status Bar Integration**
   - The notification will be displayed in the VS Code status bar for easy visibility without disrupting the user interface.

2. **Logic for Determining Visibility**
   - Use Git commands or APIs to retrieve the remote URL.
   - Check if the remote URL corresponds to a public or private GitHub repository using GitHub's API or other methods.

3. **URL Conversion**
   - Strip `.git` from the end of the remote URL to make it browser-accessible.

4. **Error Handling**
   - Handle cases where:
     - The repository is not a GitHub repository.
     - The remote URL is invalid or inaccessible.
     - API rate limits are exceeded.

---

## **Future Enhancements**
- Support for repositories with multiple remotes.
- Compatibility with submodules.
- Notifications for other Git hosting platforms (e.g., GitLab, Bitbucket).
- Customizable notification placement (e.g., pop-ups, sidebars).

 