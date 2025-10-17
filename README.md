**YouTube Nifi Pipelines**

This project implements a modular data pipeline to extract and process YouTube channel and video data using Nifi. The pipeline automates the collection, transformation, and storage of channel and video information into a relational database.

**Pipeline Workflow**

  **1. Channel URL Extraction**
    Fetches unprocessed channel URLs from the table and checks if they contain a channel_id.

  **2. Channel ID Retrieval**
    Extracts channel_id via API if missing and stores it in the channel_ids table.

  **3. Channel Data Collection**
    Retrieves detailed channel information using the channel_id and stores it in the channels table.

  **4. Video Data Collection**
    Fetches the upload playlist for each channel, retrieves videos in batches (max 50 per API call), and handles pagination to capture all videos.

  **5. Video Data Storage**
    Collects detailed video information for each video ID and stores it in the videos table.

    

**Key Features**

Modular design for separate handling of channels and videos.

Automatic extraction of channel_id from URLs.

Efficient API pagination for large playlists.

Structured storage in relational tables (channels, channel_ids, videos) for easy querying.

