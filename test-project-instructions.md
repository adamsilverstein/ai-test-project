# Test Project Instructions

## Objective
The objective of this project is to build a new WordPress block plugin that provides a custom Weather block. This block will allow users to display current weather information for a specified location.

## Requirements
1. The plugin must be built using the latest WordPress standards and best practices.
2. The Weather block must be customizable, allowing users to specify the location for which they want to display weather information. The user can also choose a light mode, dark mode or auto mode for the block display.
3. The block must fetch weather data from a reliable weather API and display it in a user-friendly format.
4. The plugin must include proper error handling for API requests and log any error messages.

## Technical Specifications
- Use the WordPress Block Editor (Gutenberg) for creating the block.
- The plugin will be primarily weritten in JavaScript (Preact) for the block display. The PHP will be used for server-side rendering and API requests.
- All data should be cached both server and client side to avoid extra requests to the server and the weather API.
- All PHP should pass the PHPCS WordPress Coding Standards.
- All PHP should pass PHPStan level 5.
- The plugin should include unit tests that covers a large percentage of the codebase.
- The plugin should include visual regression tests that verify that the block renders correctly given correct data.
- The codebase should be well-documented, with inline comments explaining complex logic and a README file that provides an overview of the plugin and its usage.
- The plugin should include GitHub actions for continuous integration, including linting, testing, and visual regression testing.

## Deliverables
1. A fully functional WordPress plugin that meets the above requirements.
2. A README file that explains how to install and use the plugin.
3. A series of clear, feature specific commits that document the development process, including any challenges faced and how they were overcome.


## Notes
- The current folder is already connected to a GitHub repository.
- Ensure that all code is committed to the repository with clear commit messages.
- Break down the task of building the plugin into smaller, manageable tasks and create branches or issues in the GitHub repository for each task.
- WordPress coding standards: https://developer.wordpress.org/coding-standards/wordpress-coding-standards/
- PHPStan documentation: https://phpstan.org/user-guide/getting-started
- Block editor handbook: https://developer.wordpress.org/block-editor/
- For the weather API, consider using OpenWeatherMap or a similar service that provides a free tier for development purposes.
- Ensure that the plugin is compatible with the latest version of WordPress and follows best practices for security and performance.
- Consider accessibility standards when designing the block to ensure it is usable by all users.
