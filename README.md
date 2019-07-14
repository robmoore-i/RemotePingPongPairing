# Remote ping-pong pairing

### Flow

1. I am pairing remote with my partner.

2. I want my partner to take over, but we have lots of WIP (I disappove).

3. I run `./ping rob`

- This puts my WIP onto a branch called and pushes it.

- I am responsible for deleting my local copy of the branch.

4. My partner runs `./pong rob`

- This fetches the remote WIP branch, and applies the change-list to their
  current branch without effecting the version control history.

- It then deletes the WIP branch

5. At this point my partner has an uncommited change-list equal to the
   change-list I had on my machine before I ran a 'ping'. We continue
   working as though nothing happened.

6. (Optional) My partner reminds me to delete my local copy of the WIP branch.

### Recommended usage

1. Clone this repository somewhere
2. Add it to your path.

### FAQ

-  Why does the local copy of WIP branch not get deleted on the creator side?

If, God forbid, something goes wrong, I would not like errors in my script to be
responsible for erasing WIP.

- Why do I pass my name to the script?

It doesn't actually matter what you pass - it needs to be some identifying word
that you and your partner both put into the scripts. I could, feasibly, make it
so that the script uses some formatting of the date as the remote branch id, but
then that could be annoying because you'd have to watch out for boundary conditions.
