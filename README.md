Builds the Censorship.no website using Hugo and Git.

# Usage 
Hugo is required - you can install Hugo using the following:

`sudo apt-get install hugo`

For Mac users:

`brew install hugo`

Clone the repo, which will become a subdirectory of the directory of your choosing:

`git clone git@github.com:censorship-no/ceno-website.git`

Move into the ceno-website directory and enable the Ananke theme's Git submodule using:

`git submodule update --init --recursive`

Run the following to serve the site locally via http://localhost:1313:

`hugo server -D`
