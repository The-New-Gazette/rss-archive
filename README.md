# Preserve This Podcast

## About
This is an RSS archive of publications from [The New Gazette](https://newgazette.co), a service providing curated and unbiased local news. 

## Acknowledgement
This page was based off of the codebase for [preservethispodcast.org](http://preservethispodcast.org/), a [Andrew W. Mellon grant-funded project](https://mellon.org/grants/grants-database/grants/new-york-metropolitan-reference-research-library-agency/1711-05080/) to preserve podcasts for future listeners.

## Customize
   * `_data / content.yml` controls text and links displayed on the homepage/front end, including:
      * Google Analytics
      * URLs for buttons throughout the sections of the website
      * URLs to subscribe to each podcatchers
      * Individual episode title
      * URL to RSS streaming and downloadable audio from podcast hosting platform
      * URL to each exercise in zine page corresponding to each episode
      * URL to each episode transcript
      * Metadata to upcoming events
      * Metadata to past events
   * `_episodes` includes individual markdown files per episode. This will hold metadata for the RSS feed to loop through. Each episode will have its own markdown file. Each of these fields need to have valid metadata.
      * `layout: post` (this will always be “post”)
      * `title:` (the value must be in quotations)
      * `file:` (this is the URL to the MP3 file from Internet Archive. [Directions on getting mp3 file URL] (https://turbofuture.com/internet/How-to-Host-Podcast-Audio-on-Archiveorg))
      * `file_itunes:` (this is the URL to the MP3 file that will be sent to Apple Podcasts)
      * `excerpt:` (this is the show notes)
      * `summary` (show notes again)
      * `duration` (audio length in minutes within quotations)
      * `length` (file size in bytes within quotations)
      * `explicit` (yes or no within quotations if there is explicit language)
      * `block` (yes or no within quotations if you’d like to display the podcast in itunes)
      * `categories:` (the value will always be “episodes” but not within quotations)
   * `_includes / footer.html` controls the text that appears at the footer of the website. In this case, this credited our sponsors, website developer, and the Creative Commons license that identifies what rights people have when using our podcast, accompanying text/images, etc. 
   * `_includes / header.html` controls the title and URLs for the header navigation bar/menu.
   * `assets / images` all image files you want to appear on the website will live in this folder.
   * `pages / 404tba.html` controls the 404 error page that visitors see when something is broken. Customize it to your style 
   * `pages / about.html` controls the About page. Shout-out to all the players and creators.
   * `transcripts` this folder holds each episode transcript 
   * `transcripts / trancript01-time-to-take-notice.md` this is the individual episode trancript. Be sure to write this in markdown and to settle on a standard and orderly naming convention for the consecutive transcript files.
   * `_config.yml` holds the website builder, Jekyll Configurations. You’ll need to personalize the website by adding your `title`, `description`, `url`. Keep `baseurl` as just the quotes.
   * `index.html` the core of the website
   * `podcast.rss` Go through the XML code and find places where you can customize it to your show. For example:
      * Line 30: `<itunes:image href="{{ site.url }}/assets/images/PTP_logo_itunes.png" />` Swap in the png file name of your logo image file
      * Lines 31-36: insert your own categories that match Apple’s vocabulary As of Aug. 2019, here are the [available categories](https://9to5mac.com/2019/08/01/apple-podcasts-categories/).
      * Line 52: `<itunes:image href="{{ site.url }}/assets/images/PTP_logo_itunes.png" />` Again, swap in the png file name of your logo image file

Don’t forget to
   * test your RSS before submitting to podcatchers : [Podbase](https://podba.se/validate/)
