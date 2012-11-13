tm
==

`tm` provides a convenience layer around `tmux`

Basic usage
-----------

 * `tm` - list current sessions.
 * `tm foo` - attach to session `foo`, creating it if it doesn't exist.

Cloning and sharing sessions
----------------------------

 * `tm -x foo`  Normally if you attach to the same session `foo` twice
    both clients share _all_ of their state.  If you change windows in
    once client, the other follows.  Sometimes while pair working this
    can be very convenient; other times you want two clients to be able
    to work individually in a shared set of windows.

    The `-x` option allows the independant movement described above
    by creating a temporary copy of the named session, which is
    automatically destroyed after the client disconnects.

 * `tm -b bar foo`  Similarly to the `-x` option above, this creates
    a second session `bar` that shares the windows and and panes of the
    first (`foo`).  Unlike `-x`, the second session is not
    automatically destroyed.
