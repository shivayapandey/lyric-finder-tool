# Lyrics Finder Tool using OpenAGI and Serper API

This README provides detailed instructions for setting up and using a Custom Lyrics Finder Tool, which leverages OpenAGI and the Serper API to search for song lyrics based on the artist and song title.

## Setup Instructions

### Restart the Colab Session
It's important to restart the Colab session before running any code to prevent dependency issues. This can be done from the "Runtime" menu by selecting the "Restart runtime" option. Once the session is restarted, you should run all cells from the beginning.

### Install Required Packages
The tool requires specific packages to function. These packages should be installed by running the appropriate commands in a code cell within the notebook.

### Set Up API Keys
You will need to set up your OpenAI API key by assigning it within the code. This key is crucial for accessing the OpenAI services required by the tool.

## LyricsFinderTool Class

The `LyricsFinderTool` class is a custom tool designed specifically for searching song lyrics. It uses the Serper API to perform searches based on the provided artist and song title. The tool is built with an `execute` method that constructs a search query and retrieves relevant lyrics by communicating with the Serper API. If lyrics are found, they are returned in a formatted, easy-to-read manner; otherwise, a message indicating that no lyrics were found is provided.

## Worker Setup

A specialized worker is created for song information retrieval. This worker is designed with a specific role and set of instructions to focus on finding and retrieving lyrics based on user queries. The worker utilizes the `LyricsFinderTool` to perform the searches and ensures that the lyrics are accurate and presented in a user-friendly format.

## Admin Setup

The Admin is configured to manage the worker and execute tasks. The setup includes utilizing OpenAI's language model for natural language processing and assigning the worker to handle specific queries related to song lyrics. The Admin also handles the overall orchestration of the tool's operations, including planning tasks and managing worker interactions.

## Execution

The tool is executed by running the Admin with a specific query that requests song lyrics. The Admin processes the query, coordinates with the worker, and returns the song lyrics formatted with clear separation of verses and choruses. This process demonstrates the full functionality of the Lyrics Finder Tool.

## Conclusion

This notebook provides a comprehensive setup for a Custom Lyrics Finder Tool using OpenAGI and the Serper API. By following the instructions outlined in this README, you can successfully implement and use the tool to retrieve song lyrics based on the artist and song title. The tool is designed to be user-friendly, accurate, and efficient, making it a valuable resource for music enthusiasts and developers alike.
