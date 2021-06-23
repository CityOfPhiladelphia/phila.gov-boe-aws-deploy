# Board of Ethics file management

## Purpose

The Board of Ethics uses a series of interconnected PDFs to manage documents through SharePoint. This functionality is not available on the WordPress platform, and due to timeline constraints will not be able to be replicated in time for a June 14th 2021 SharePoint shutdown date. This repo facilitates the direct upload of PDFs to specific Ethics Board public folder paths, so that old PDFs will not be lost, and new PDFs can be maintained in the short term.

## How to use

1. Use the GitHub interface to upload a new file to the default (staging) branch. 
2. After a successful deploy to staging (e.g. https://staging-www.phila.gov/ethicsboard/Advisory%20Opinions/bd.op.2006-001.pdf) create Pull Request into `main`. 
3. Merge pull request to publish file(s). 
