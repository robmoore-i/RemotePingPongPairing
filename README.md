# Remote ping-pong pairing

## Desired Flow

1. I am pairing remote with my partner.

2. I want my partner to take over, but we have lots of WIP (very naughty).

3. I run `./ping rob`

- This puts my WIP onto a branch and pushes it.

- I am responsible for deleting my local copy of the branch.

4. My partner runs `./pong rob`

- This fetches the remote WIP branch, and applies the change-list to the
current branch, but without effecting the version control history.

- It then deletes the WIP branch

5. My partner continues working

## Current Flow

1. I am pairing remote with my partner.

2. I want my partner to take over, but we have lots of WIP (very naughty).

3. I run `./ping rob`

- This puts my WIP onto a branch and pushes it.

- I am responsible for deleting my local copy of the branch.

4. My partner runs `./pong rob`

- This fetches the WIP branch and rebases it onto the current branch (should be master)

- It then deletes the WIP branch

5. My partner continues working
