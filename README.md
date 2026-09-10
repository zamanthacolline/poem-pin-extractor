# Poem Pin Extractor

A lightweight, automated Python script that processes lists of text poems to extract hidden numeric security pins or keys based on dynamic word-length mappings relative to structural line indexes.

## Project Structure

The project directory contains the core script along with environment and integration modules:
- main.py - Contains the core pin_extractor function and execution driver
- debuggee.py - Environment configuration scripts
- handlers.py - Input event routines
- output.py - Stream logs and storage handles
- winapi.py - Internal platform integration

## How It Works

The core logic evaluates text strings systematically using text offsets:
1. Splits strings into discrete lines via newline boundaries.
2. Iterates over line indexes while counting individual word occurrences.
3. If the total number of words on a given line exceeds its zero-based structural index threshold, it extracts the length of the specific word located at that index.
4. If the words are shorter than the index threshold, it defaults to inserting a structural padding zero.

## Installation

Ensure you have Python installed on your local environment.

## Usage

Execute the program entry point directly from your system console:
python main.py
