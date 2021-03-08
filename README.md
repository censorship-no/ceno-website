Builds the Censorship.no website using Hugo and Git.

=Usage=
Hugo is required - you can install Hugo using the following:
`sudo apt-get install hugo`

You will also need to enable the Ananke theme's Git submodule using:
`git submodule update --init --recursive`

Clone the repo and run the following to serve the site locally via localhost:1313:
`hugo server -D`
