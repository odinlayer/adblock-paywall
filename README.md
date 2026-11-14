# OdinLayer AdBlock & Paywall

A lightweight, custom filter list for **Adblock Plus (ABP)**, designed to block unwanted advertising, tracking, and paywall-related resources.

The project focuses on targeted filtering rules to minimize website breakage while improving the browsing experience.

## Features

- Designed for Adblock Plus.
- Uses Adblock Plus-compatible filtering syntax.
- Blocks selected advertising and paywall-related scripts.
- Targeted URL filtering instead of unnecessary domain-wide blocking.
- Organized by website for easy maintenance.
- Supports exceptions and custom filtering rules.
- Regularly updated as new rules are added.

## Installation

### Adblock Plus

1. Install [Adblock Plus](https://adblockplus.org/) in your browser.
2. Open **Adblock Plus Settings**.
3. Navigate to **Advanced**.
4. Under **Filter lists**, select **Add a new filter list**.
5. Enter the following subscription URL:

   ```
   https://raw.githubusercontent.com/odinlayer/adblock-paywall/main/filters.txt
   ```

6. Confirm to add the filter list.

Adblock Plus will periodically check for updates to the list.

## Filter Rules

All filtering rules are maintained in [`filters.txt`](./filters.txt).

### Syntax Examples

| Purpose | Example |
|---------|---------|
| Block a specific URL | `||example.com/path/file.js` |
| Block JavaScript | `||example.com/file.js$script` |
| Block an entire domain | `||ads.example.com^` |
| Block third-party resources | `||example.com/file.js$third-party` |
| Restrict to a website | `||example.com/file.js$domain=website.com` |
| Allow a blocked resource | `@@||example.com/file.js` |

For more information, see the [Adblock Plus filter syntax documentation](https://help.adblockplus.org/hc/en-us/articles/360062733293-How-to-write-filters).

## Adding New Rules

1. Open `filters.txt`.
2. Find the section for the relevant website, or create a new section.
3. Add one filtering rule per line.
4. Test the rule with Adblock Plus.
5. Update the version and modification date.
6. Commit and push your changes.

Example:

```text
! --- Example Website ---

||example.com/assets/advertisement.js$script
||cdn.example.com/tracker.js$script
```

## Compatibility

This filter list is primarily maintained and tested for **Adblock Plus**.
Other content blockers may support some or all of the rules, but compatibility is not guaranteed.

## Contributing

Contributions, suggestions, and bug reports are welcome.

1. Fork this repository.
2. Create a branch for your changes.
3. Add or update rules in `filters.txt`.
4. Test your rules using Adblock Plus.
5. Submit a pull request describing your changes.

If a rule causes website breakage, please open an issue with the affected website and the rule responsible.

## Disclaimer

This project provides custom filtering rules for Adblock Plus.

- Some websites may not function correctly when certain resources are blocked.
- Filtering behavior may vary depending on browser and Adblock Plus version.
- Blocking paywall-related scripts does not guarantee access to restricted content.
- Users are responsible for complying with applicable website terms and laws.

