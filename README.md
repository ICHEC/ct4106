
# CT4106
[![deploy-book](https://github.com/ICHEC/CT4106/actions/workflows/publish.yml/badge.svg)](https://github.com/ICHEC/CT4106/actions/workflows/publish.yml)

## Structure
```mermaid
graph LR
Old("External") ==> New(["CT4106"])
1o(Lecture 1) ==> 1n(Lecture 1)
2o(Lecture 2) ==> 2n(Lecture 2) 
3o(Lecture 3) ==> 3n(Lecture 3)
new1("New") ==> 4n(Lecture 4)
new2("Guest 1") ==> 5n(Lecture 5)
4o(Lecture 4) ==> 6n(Lecture 6)
new3("Guest 2") ==> 7n(Lecture 7)
5o(Lecture 5) & 6o(Lecture 6) ==> 8n(Lecture 8)
new4("Guest 3") ==> 9n(Lecture 9)
7o(Lecture 7) ==> 10n(Lecture 10) & 11n(Lecture 11)
new5("ICHEC") ==> 12n(Lecture 12)
```

## Developer README

To locally render the HTML for the lecture notes:

1. Create a new environment
2. Install the required packages from `requirements.txt`
3. Using homebrew, install drawio to render some of the diagrams in the notes:
```{code-cell}
brew install --cask drawio
```
4. Build the book by running the following in the root directory (where `_config.yml` and `_toc.yml` are located):
```{code-cell}
jupyter-book build .
```
5. Copy and paste the generated link into a browser to view the notes.
