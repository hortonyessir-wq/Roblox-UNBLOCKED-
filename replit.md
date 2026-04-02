# Roblox Login Bot

A Python console application that automates login to Roblox using Selenium with Firefox (geckodriver).

## Overview

This script prompts the user for their Roblox username and password, encodes them using a custom character mapping, saves them to `encryption.txt`, and then automates a login to the Roblox website.

## Project Structure

- `main.py` - Entry point; handles user input, credential saving, and Selenium automation
- `encryption.py` - Custom encoding/decoding module using character index mapping
- `encryption.txt` - Stores encoded credentials
- `pyproject.toml` - Poetry dependency management

## Dependencies

- **Python 3.8**
- **selenium ^4.1.0** - Browser automation
- **geckodriver** - Firefox WebDriver (installed via Nix)

## Running the App

The app runs as a console workflow. When started, it will:
1. Prompt for a username and password
2. Save encoded credentials to `encryption.txt`
3. Open a headless Firefox browser and attempt to log in to Roblox

## Notes

- Uses Firefox (geckodriver) instead of Chrome, as geckodriver is available in the Nix environment
- The browser runs in headless mode
- The "encryption" is a simple character-to-index mapping and is NOT cryptographically secure
