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
# Splinter Glossary

<h3 class="glossary-header">
Biome
</h3>

<p class="glossary-definition">
Biome is a module in libsplinter containing several submodules that provide
support for user management, user credential management, and private key
management.
</p>

<h3 class="glossary-header">
Canopy
</h3>

<p class="glossary-definition">
Application interface for Splinter that can provide apps dynamically.
Canopy is a distributed-application UI framework that dynamically loads saplings
(application UI components) based on circuit configuration, user permissions,
and enterprise requirements.
</p>

<h3 class="glossary-header">
circuit
</h3>

<p class="glossary-definition">
Virtual network within the broader Splinter network that safely and securely
enforces privacy scope boundaries. A circuit defines the scope and visibility
domains for two or more connected organizations.
</p>

<h3 class="glossary-header">
consensus
</h3>

<p class="glossary-definition">
Mechanism for ensuring agreement between Splinter services and
<a class="tooltip">nodes<span class="tooltiptext">{{site.data.glossary.node}}</span></a>.
Splinter currently supports two-phase commit consensus, a basic consensus algorithm
that requires all participating parties to agree. (Other algorithms are planned for
the future.)
</p>

<h3 class="glossary-header">
node
</h3>

<p class="glossary-definition">
Foundational runtime software that allows an organization to participate
in the network.
</p>

<h3 class="glossary-header">
sapling
</h3>

<p class="glossary-definition">
Plug-in app for Canopy that can customize the UI, access Splinter or external
functionality, or communicate with back-end platforms and software.
Splinter includes a growing set of reusable saplings for common functionality
and interfaces with related products.
</p>

<h3 class="glossary-header">
Sawtooth Sabre
</h3>

<p class="glossary-definition">
Smart contract engine: A distributed application that implements on-chain smart
contracts that can be executed in a WebAssembly virtual machine.
</p>

<h3 class="glossary-header">
scabbard
</h3>

<p class="glossary-definition">
Splinter service that runs Sawtooth Sabre smart contracts across nodes,
coordinated with consensus.
</p>

<h3 class="glossary-header">
service
</h3>

<p class="glossary-definition">
Endpoint within a circuit that sends and receives private messages.
</p>

<h3 class="glossary-header">
shared state
</h3>

<p class="glossary-definition">
Distributed database that is visible only to the services within a circuit.
Shared state is updated by smart contracts.
</p>

<h3 class="glossary-header">
smart contract
</h3>

<p class="glossary-definition">
Business logic that processes transactions. Runtime deployment of smart
contracts by the scabbard service means no need to upgrade the Splinter software
stack to add business logic. Sandboxed WebAssembly smart contracts keep the
network safe and ensure determinism.
</p>

<h3 class="glossary-header">
splinterd
</h3>

<p class="glossary-definition">
Splinter daemon that handles internal functionality such as circuit creation and
management, consensus, and service coordination.
</p>

<h3 class="glossary-header">
state delta export
</h3>

<p class="glossary-definition">
Mechanism that provides changes to shared state as "state deltas" (state-change
updates from Splinter as a result of processed transactions).
Applications can subscribe to these changes to get current information that can
be stored in a local database.
</p.
