# Public Or Private Repo Extension (WIP, VS Code Extension)

## Purpose Statement

For users who create many Github repositories (ahem) It's convenient to be able to create both public and private repos. 

Sometimes private repositories are used for private projects that should not be shared publicly, or which may contain data that is not intended for public distribution such as collections of personal scripts or those for an internal business use. Sometimes people create both private and public repositories for projects, using a private repository to test ideas and a public repository only when it's ready for being shared. 

The only problem is that as your collection of repository scales, it can become challenging to remember which repositories are public and which are private without having to manually check the remotes every time. While there are some solutions, such as using a specific naming convention for private repositories sometimes it would just be nice to have a notification in VS Code to remind you whether the repository you're working on is private or public. This would enhance security by providing a visual reminder to users as to which type of repository they're working in preventing the accidental publishing of personal information. 

The idea for this project is creating a simple VS code extension which determines whether the repository is public or private and then provides a simple visual indicator as outlined above.  

## Feature Plan

### Visual Indicator

Visual indicator warning light system providing at-a-glance indication as to whether the repo is public or private. 

### View Remote Repo

As an additional complementary feature, the ability to open the detected remote repository in the browser. This would require a little bit of text editing logic to convert the standard URL for remote repositories into one that can be opened in a web browser. 

## Color Scheme / UI / Iconography

Although it seems sensible to use a "green is public" and "red is private" color scheme, that UI actually runs contrary to the objective. For this particular use case, users would wish to be reminded that the repository they're working on *is* public so as to make sure not to commit private information there ... and red is the typical color association for warning messages. Some thought will have to be put into this about the most appropriate choice of emoji or icon or color. 

## Advanced Feature Ideas

### Submodule Handling

The plan for the first version is just to handle simple notifications for basic repositories. But down the line thought might want to be invested into how to handle sub modules.

### Multiple Remote Handling

Additionally, the repository may wish to handle the case in which a repository has multiple remotes configured. In this case, various methodologies could be employed and the warning system could perhaps be configured by the user. For example:

- Notify me if *any* of the remotes are public. 
- If any of the remotes are public, provide the URL and the notification and a count. For example, "this local repository is associated with 2 public remotes."
 

## Author

Daniel Rosehill  
(public at danielrosehill dot com)

## Licensing

This repository is licensed under CC-BY-4.0 (Attribution 4.0 International) 
[License](https://creativecommons.org/licenses/by/4.0/)

### Summary of the License
The Creative Commons Attribution 4.0 International (CC BY 4.0) license allows others to:
- **Share**: Copy and redistribute the material in any medium or format.
- **Adapt**: Remix, transform, and build upon the material for any purpose, even commercially.

The licensor cannot revoke these freedoms as long as you follow the license terms.

#### License Terms
- **Attribution**: You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
- **No additional restrictions**: You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.

For the full legal code, please visit the [Creative Commons website](https://creativecommons.org/licenses/by/4.0/legalcode).