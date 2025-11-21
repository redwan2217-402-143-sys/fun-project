# fun-project
fun project . project-1
only work on linux
if you wanna make it multi os than use this 
#!/bin/bash

url=".........."

open_url() {
    case "$OSTYPE" in
        linux*)   xdg-open "$url" ;;
        darwin*)  open "$url" ;;
        msys*)    start "$url" ;;   # Git Bash/Windows
        cygwin*)  start "$url" ;;
        *)        echo "Unsupported OS" ;;
    esac
}

open_url
