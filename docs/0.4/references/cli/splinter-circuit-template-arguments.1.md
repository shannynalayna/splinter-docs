% SPLINTER-CIRCUIT-TEMPLATE-ARGUMENTS(1) Cargill, Incorporated | Splinter Commands
<!--
  Copyright 2018-2020 Cargill Incorporated

  Licensed under the Apache License, Version 2.0 (the "License");
  you may not use this file except in compliance with the License.
  You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

  Unless required by applicable law or agreed to in writing, software
  distributed under the License is distributed on an "AS IS" BASIS,
  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  See the License for the specific language governing permissions and
  limitations under the License.
-->

NAME
====

**splinter-circuit-template-arguments** — Displays the arguments defined in a
circuit template

SYNOPSIS
========
**splinter circuit template arguments** \[**FLAGS**\] TEMPLATE-NAME

DESCRIPTION
===========
Circuit templates help simplify the process of creating new circuits with the
`splinter circuit propose` command. Circuit template arguments are required when
building a circuit from the template. This command lists the arguments that are
defined in the specified circuit template.

FLAGS
=====
`-h`, `--help`
: Prints help information

`-q`, `--quiet`
: Decrease verbosity (the opposite of -v). When specified, only errors or
  warnings will be output.

`-V`, `--version`
: Prints version information

`-v`
: Increases verbosity (the opposite of -q). Specify multiple times for more
  output.

ARGUMENTS
=========
`TEMPLATE-NAME`
: Circuit template that contains the arguments of interest.

EXAMPLES
========
The following command shows the arguments for the `scabbard` circuit template,
which is available by default (packaged with the Splinter CLI).

```
$ splinter circuit template arguments scabbard

name: admin_keys
required: false
default_value: $(a:SIGNER_PUB_KEY)
description: Public keys used to verify transactions in the scabbard service

name: nodes
required: true
default_value: Not set
description: List of node IDs

name: signer_pub_key
required: false
default_value: Not set
description: Public key of the signer
```

SEE ALSO
========
| `splinter-circuit-template-list(1)`
| `splinter-circuit-template-show(1)`
|
| Splinter documentation: https://github.com/Cargill/splinter-docs/blob/master/docs/index.md
