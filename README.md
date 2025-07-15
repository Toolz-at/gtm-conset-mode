
# Consent Mode Banner Template

This repository contains the Consent Mode Banner template for Google Tag Manager (GTM), using the free tool provided by [Toolz.at](https://toolz.at/).

## Description

The template implements functionalities to manage user consent states, set default consent modes, and inject the required script to display the consent banner.

## Features

- Default consent state configuration.
- Stores consent information in `localStorage`.
- Integration with Google Tag Manager.
- Dynamically injects scripts with verified permissions.
- Granular management of consent categories:
  - **Necessary**: `functionality_storage`, `security_storage`.
  - **Marketing**: `ad_storage`, `ad_user_data`, `ad_personalization`.
  - **Analytics**: `analytics_storage`.
  - **Preferences**: `personalization_storage`.

## Dependencies

- [Toolz.at Consent Management Platform](https://toolz.at/) library.

## Code Structure

The main file includes the following functions and methods:

- **`setDefaultConsentState`**: Sets the default consent state.
- **`updateConsentState`**: Updates the consent state based on user interaction.
- **`getCookieValues`**: Retrieves cookie values related to consent.
- **`gtagSet`**: Configures optional Google Analytics settings, such as:
  - `ads_data_redaction`
  - `url_passthrough`
  - `developer_id`
- **`queryPermission`**: Checks permissions before executing script injection.
- **`injectScript`**: Injects the consent banner script.

## Setup Instructions

1. Download the code from this repository.
2. Replace the placeholder values in the code with your specific settings.
   - Configure `data.consetModeID` with your banner ID.
3. Ensure all required functions and libraries are properly configured in your GTM environment.
4. Upload the script to Google Tag Manager as a custom tag template.

## Usage

- The script automatically initializes when loaded in GTM.
- It checks the current consent state and applies the default configuration.
- If no consent is stored, it sets the consent states as per the default settings.

## References

For more information, refer to the official documentation at [consentmode.toolz.at](https://consentmode.toolz.at).

---

**Note**: This project was developed as a free solution to manage consents in GTM. Contributions are welcome.
