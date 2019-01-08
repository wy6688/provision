drpcli bootenvs fromAppleNBI
============================

This will attempt to translate an Apple .nbi directory into a bootenv
and an archive.

Synopsis
--------

This command translates an Apple .nbi directory into a bootenv .yaml
file that contains apropriate metadata to be handled by the dr-provision
NBSP DHCP handler, and a .tar.gz file that contains the contents of the
.nbi directory.

The .nbi directory must have been produced by the Apple System Image
Utility or equivalent tooling, and must contain a valid
NBImageInfo.plist file. The .yaml file containig the bootenv will be
named -.yaml, and the .tar.gz file will contain the contents of the .nbi
directory.

Both created files will be left in the current working directory.

::

    drpcli bootenvs fromAppleNBI [path] [flags]

Options
-------

::

      -h, --help   help for fromAppleNBI

Options inherited from parent commands
--------------------------------------

::

      -d, --debug               Whether the CLI should run in debug mode
      -E, --endpoint string     The Digital Rebar Provision API endpoint to talk to (default "https://127.0.0.1:8092")
      -f, --force               When needed, attempt to force the operation - used on some update/patch calls
      -F, --format string       The serialzation we expect for output.  Can be "json" or "yaml" (default "json")
      -P, --password string     password of the Digital Rebar Provision user (default "r0cketsk8ts")
      -r, --ref string          A reference object for update commands that can be a file name, yaml, or json blob
      -T, --token string        token of the Digital Rebar Provision access
      -t, --trace string        The log level API requests should be logged at on the server side
      -Z, --traceToken string   A token that individual traced requests should report in the server logs
      -U, --username string     Name of the Digital Rebar Provision user to talk to (default "rocketskates")

SEE ALSO
--------

-  `drpcli bootenvs <drpcli_bootenvs.html>`__ - Access CLI commands
   relating to bootenvs