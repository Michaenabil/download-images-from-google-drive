# Google Drive Image Downloader

## Overview

This PowerShell script automates downloading images from a list of Google Drive links stored in a text file. It is especially useful when working with bulk media download tasks, such as labeling datasets or backing up shared images.

## Features

- Parses various Google Drive URL formats (direct links, share links, etc.)
- Saves downloaded images with **odd-numbered sequential filenames** (`1.jpg`, `3.jpg`, ...)
- Customizable options for output directory, filename prefix, and timeout settings
- Includes error handling for inaccessible links or failed downloads

## Requirements

- PowerShell 5.1 or newer
- Internet connection
- Access permissions to the linked Google Drive files

## Configuration

Modify the `$config` hashtable at the beginning of the script to set:

```powershell
$config = @{
    InputFile     = "C:\path\to\your\input.txt"
    OutputFolder  = "C:\path\to\save\images"
    FilePrefix    = "image_"
    StartNumber   = 1
    Increment     = 2
    FileExtension = ".jpg"
    TimeoutSec    = 30
}
