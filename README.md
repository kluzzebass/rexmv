USAGE: rexmv -m <match> -r <replacement> [-f] [items ...]
  -m <match>       : regexp matching pattern (may include grouping parentheses).
  -r <replacement> : use $1, $2 and so on to reference grouping from the matching pattern.
  -f               : actually rename the items, instead of just dry running.

Examples:

  Make everything upper case:

    rexmv -m '(.*)' -r '\U$1' *

  Change extension from .mp4 to .mpeg4:

    rexmv -m '.mp4$' -r '.mpeg4' *

  Change '1of8' to 'S01E01', '2of8' to 'S01E02' and so on (useful for renaming tv show episodes):

    rexmv -m '(\d+)of8' -r 'S01E0$1' *

