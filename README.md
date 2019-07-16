anonacount -- create anonymous usser login/email accounts for users in Ubuntu
(C) Copyright Herbert J. Bernstein 2019
This software may be released under the GPL 2.0
See LICENSE

The software uses a file named gemstones as a source of names
to which it appends one or more digits to make each new name unique.
The names are generated with a scripts make_new_name, which should
be stored in /sbin with permission 500, so it can only be read
or run by root.

  make_new_name namelist onamelist
    returns a name from namelist followed by a number
    such that the new name does not appear in onamelist
    onamelist defaults to /etc/passwd

The top level script to run is

  make_bulk_anon N
    makes N+1 anonymous email accounts and sends instructions to the first one
    as the instructor handing the block

This script should be edited to send the final emails to the appropriate addresses
to receive instructions on use of the generated accounts.



