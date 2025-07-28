# AI Agent Test: WordPress Weather Block Plugin

## 🎯 Objective

The objective is to build a WordPress block plugin that provides a custom "Weather Block". This block will display current weather conditions for a user-specified location, fetched from a live API.

-----

## 🚀 Getting Started

1.  **Scaffolding:** Use the official `@wordpress/create-block` tool to generate the initial plugin structure. Name the block `weather-block`.
2.  **API Key:** For the weather API, use the **OpenWeatherMap API**. You will be provided with an API key. **Do not hardcode the API key in the code.** It should be managed as a constant in `wp-config.php` or through a settings field. For this test, you can define it as a constant within the main plugin PHP file.
    ```php
    // For testing purposes, define the key here.
    // In a real plugin, this would be in wp-config.php or a settings page.
    define( 'WEATHER_BLOCK_API_KEY', 'your_provided_api_key_here' );
    ```

-----

## ✅ Requirements

### Block Controls (Editor Settings)

The block must have the following controls in the editor sidebar:

1.  **Location (`TextControl`):** An input field for the user to enter a city name (e.g., "New York").
2.  **Units (`ToggleControl` or `RadioControl`):** A control to switch between Celsius and Fahrenheit.
3.  **Display Mode (`RadioControl`):** Options for Light, Dark, and Auto modes. The "Auto" mode should respect the user's device or browser preference.

### Block Display (Frontend)

The block must display the following information:

  * City Name
  * Current Temperature (in the selected unit)
  * A weather icon representing the current conditions (e.g., ☀️, ☁️, 🌧️).
  * A short weather description (e.g., "Clear sky," "Few clouds").
  * Humidity percentage.

### Error Handling

  * If the API request fails or the location is not found, the block should display a user-friendly error message (e.g., "Could not fetch weather data. Please check the location and try again.").
  * All API errors must be logged using the standard WordPress `error_log` function.

-----

## 🛠️ Technical Specifications

  * **Technology:** Use the WordPress Block Editor (Gutenberg) with **Preact** (or React) for the editor and frontend block view. Use **PHP** for the server-side rendering fallback and API interactions.
  * **API Caching:** API responses must be cached on the server-side using the **WordPress Transients API** with a **15-minute** expiration time to minimize API calls.
  * **Security:**
      * All API requests from the WordPress admin (e.g., for a block preview) must be authenticated using **nonces**.
      * All output must be properly escaped (e.g., using `esc_html`, `esc_attr`).
  * **Coding Standards:**
      * All PHP code must pass `PHPCS` with the `WordPress` ruleset.
      * All PHP code must pass `PHPStan` at **level 5**.
  * **Internationalization:** All user-facing strings in both PHP and JavaScript must be translatable using the standard WordPress functions (`__()`, `_e()`, `wp.i18n.__`, etc.).
  * **Testing:**
      * **Unit Tests:** PHP and JavaScript unit tests are required, aiming for **\>80% code coverage**. Focus on testing API data handling and data transformation logic.
      * **Visual Regression Tests:** Include at least one visual regression test using **Playwright** to verify the block renders correctly in its default state.
  * **Documentation:**
      * Provide a `README.md` file with setup instructions (including the dependency `composer install` and `npm install`) and usage information.
      * Use inline comments to explain complex or non-obvious code sections.
  * **Continuous Integration (CI):** The repository must include a GitHub Actions workflow that automatically runs linting (PHPCS, ESLint) and all tests (PHPUnit, Jest, Playwright) on every push.
  * **Accessibility:** Ensure the block is accessible, following WCAG 2.1 AA standards. This includes proper ARIA roles, keyboard navigation, and screen reader support.
  * **Build Process:** Use `npm` for managing JavaScript dependencies and build processes. Include a command to bundle the plugin as a Zip file for distribution.

-----

## Deliverables

1.  A fully functional WordPress plugin in a `.zip` file.
2.  The complete source code pushed to the provided GitHub repository.
3.  A `README.md` file explaining installation and usage.
4.  A commit history that follows the **Conventional Commits** specification (e.g., `feat:`, `fix:`, `docs:`). This demonstrates a structured development process.

-----

## 📝 Notes

  * You have push access to the current GitHub repository.
  * Break down your work into logical, incremental commits.
  * Focus on creating a production-quality, secure, and performant plugin.
  * Ensure the block design is clean, modern, and accessible (WCAG 2.1 AA).