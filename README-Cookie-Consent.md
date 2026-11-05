# Cookie Consent Implementation for Microsite Template

This document describes the cookie consent implementation added to the microsite template, based on the implementation from the uncharted-www project.

## Overview

The microsite template now includes a comprehensive cookie consent system that:
- Manages Google Analytics cookies based on user consent
- Provides a user-friendly consent modal
- Includes cookie preference settings
- Follows privacy best practices

## Technology Used

We use [Cookie Consent by orestbida](https://github.com/orestbida/cookieconsent) for the cookie consent functionality.

## Implementation Details

### Files Modified

1. **`/themes/uncharted-microsite/layouts/partials/head.html`**
   - Added Cookie Consent CSS
   - Added custom Uncharted theme styling
   - Replaced Hugo's internal Google Analytics with cookie consent-aware implementation

2. **`/themes/uncharted-microsite/layouts/_default/baseof.html`**
   - Added Cookie Consent JavaScript
   - Added consent configuration and callbacks

3. **`/themes/uncharted-microsite/layouts/partials/footer.html`**
   - Added "Cookie Preferences" links to both desktop and mobile footer sections

### Key Features

#### Cookie Categories
- **Essential cookies**: Always enabled, required for site functionality
- **Performance cookies**: Optional, used for Google Analytics

#### Google Analytics Integration
- Google Analytics is only loaded when performance cookies are accepted
- Uses Google's consent mode API for proper consent management
- Anonymized data collection when consent is granted

#### User Interface
- Bottom-center consent modal on first visit
- "Accept all" and "Reject performance cookies" options
- Detailed settings modal with cookie information table
- Footer links to adjust preferences anytime

### Configuration

The consent modal includes:
- Links to Uncharted's privacy policy and terms of service
- Clear descriptions of cookie usage
- Cookie information table showing Google Analytics cookies
- Uncharted-branded styling matching the site theme

### Testing

To test the implementation:
1. Clear browser cookies and visit the site
2. Verify the consent modal appears
3. Test both "Accept all" and "Reject performance cookies" options
4. Check that Google Analytics loads/doesn't load based on choice
5. Use the "Cookie Preferences" link in the footer to change settings

### Privacy Compliance

This implementation:
- Provides clear information about cookie usage
- Allows users to opt-out of non-essential cookies
- Respects user choices across sessions
- Links to comprehensive privacy policy
- Uses anonymized analytics when consent is given

### Notes

- Ad blocker extensions may block Google Analytics regardless of consent
- The implementation uses the same privacy policy links as the main Uncharted website
- Cookie preferences are saved in the `cc_cookie` cookie for 6 months by default
