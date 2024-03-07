# Spotify Scraper
<div align="center">
    <picture><img width="300px" alt="librivox logo" src="https://github.com/miahj1/spotify-scraper/assets/84815985/99f64653-bacf-4642-8c11-bf47b7b7bc64"></picture>
    <div align="center"><a href="https://open.spotify.com">Homepage</a></div>
</div>
<br>

Spotify offers a vast library of music and podcasts accessible across various devices, allowing users to easily discover and enjoy content tailored to any moment.

## Python Modules
- Requests
- Pandas
- Urllib
- The Fuzz
- Time
- Typing
- Pydantic

## Summary
The client's brief asked to have book titles from Gutenberg's database of books iterated over and searched on Spotify collecting it's audibook equivalent with the following information from Spotify's API: Title, Author, Publisher, and URL. I also included a few generated columns: Similarity Score and Closest Matches. The former is a score calculated using the Levenshtein distance to find the similarity between two strings: the latter is a list of items that have the same similarity score.

Before fetching from Spotify, the Gutenberg data needed to be pre-processed:
- Removal of parentheticals `()` and brackets `[]` in the names of titles including carriage return and new lines, `\r\n`.
- Removal of `by` from the titles of the books e.g. the title would look like this for certain books `Book Title by Book Author`.
- Removal of date of birth and date of death including semicolons and commas.

The process would have to be done every month using an ETL pipeline as client requested monthly data to be compared and retrieved.

## Data Preview
A peak into what a sample of the data looks like: there were `72,000` data points collected.
<picture><img src="https://github.com/miahj1/spotify-scraper/assets/84815985/d80a4383-6d48-41b0-8dd8-e58a004dc110"></picture>

## Client Feedback
This is an ongoing effort: the client has already paid for a majority of the milestones.
