# Remove If-None-Match and If-Modified-Since Extension for Burp Suite

## Description

A Burp Suite extension that automatically removes `If-None-Match` and `If-Modified-Since` headers from HTTP requests, ensuring that cached responses do not interfere with your testing.

## Goal

The goal of this extension is to enhance web application testing by preventing servers from returning cached responses based on `If-None-Match` and `If-Modified-Since` headers.

## Installation

### Prerequisites

- Burp Suite
- Jython (for running Python extensions in Burp Suite)

### Steps

1. **Download the Jython Standalone JAR**:
   - [Jython Standalone Download](https://www.jython.org/download)

2. **Configure Jython in Burp Suite**:
   - Go to `Extender` > `Options`.
   - In the `Python Environment` section, click `Select file` and choose the downloaded Jython JAR file.

3. **Add the Extension**:
   - Go to the `Extender` > `Extensions` tab.
   - Click `Add`.
   - Set `Extension Type` to `Python`.
   - Click `Select file` and choose your Python extension file (e.g., `remove_if_none_match.py`).

4. **Verify Installation**:
   - Check the `Output` tab for a success message indicating that the extension has loaded.

## Usage

1. Open Burp Suite and go to the HTTP history tab.
2. Intercept or send HTTP requests as usual.
3. The extension will automatically remove `If-None-Match` and `If-Modified-Since` headers from all outgoing HTTP requests.

## Contributing

Contributions are welcome! Please fork the repository and submit pull requests with improvements or bug fixes.
