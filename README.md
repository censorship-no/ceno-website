Builds the Censorship.no website using Hugo and Git.

# Usage 
Hugo is required - you can install Hugo using the following:

`sudo apt-get install hugo`

Clone the repo:

`git clone git@github.com:censorship-no/ceno-website.git`

You will also need to enable the Ananke theme's Git submodule using:

`git submodule update --init --recursive`

Run the following to serve the site locally via https://localhost:1313:

`hugo server -D`
