#!/bin/bash

validate() {
    local input="$1"
    if [[ "$input" =~ ^[0-9]{4}$ ]]; then
        return 0
    else
        return 1
    fi
}

if [ $# -ne 1 ]; then
    echo "Error: Add as an input a 4-digit number"
    exit 1
fi

number="$1"

if validate "$number"; then
    echo -n "$number" | sha256sum | awk '{print $1}'
else
    echo "Error: Input is not a valid 4-digit number."
    exit 1
fi
