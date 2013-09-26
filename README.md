track-fds
=========

Scan an strace log and track where file descriptors came from

# Usage: PID=<pid> track-fds <strace-log>
#
# This will scan through the log and figure out where each file descriptor of
# pid <pid> came from. If file descriptors are closed, their original origin
# will be reported. If a file descriptor is reused for something else, then the
# previous target will be lost forever and your computer will cackle in
# merriment as you scream your frustration to the stars. That's because this is
# a total hack, and probably shouldn't be uploaded for the public to see and
# laugh at.
#
# Laugh all you want, you fools. I will show you all someday.
#
# Perhaps by allowing you to specify a line number, and reporting what was
# active at that line of the strace log? Nah, you can do that yourself already:
#
#   head -<pid> | env PID=<pid> track-fds
#
# So go away now.
