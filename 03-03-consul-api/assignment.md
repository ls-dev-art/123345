---
slug: 03-consul-api
type: challenge
title: Consul API
teaser: Use the Consul API
notes:
- type: text
  contents: |-
    Consul has a RESTful API which you can use to interact with Consul.
    You can see the see Consul API documentation [here](https://www.consul.io/api/index.html).
tabs:
- id: eahet90nbj5d
  title: Consul0
  type: terminal
  hostname: consul-server-0
- id: rfrvxvlgiwgy
  title: Consul1
  type: terminal
  hostname: consul-server-1
- id: 0xsv6fiatuog
  title: Consul2
  type: terminal
  hostname: consul-server-2
- id: aypzlr5p16ik
  title: Consul UI
  type: service
  hostname: consul-server-0
  port: 8500
difficulty: basic
timelimit: 600
enhanced_loading: null
---
Let's try some of the same commands from our last assignment with the API. We'll use the Unix `curl` command to interact with the API. Copy and paste each command into the terminal and view the output.

* Logs:
  - `curl -s http://127.0.0.1:8500/v1/agent/monitor` (CTRL-C to escape)
* List Members:
  - `curl -s http://127.0.0.1:8500/v1/agent/members | jq`
* Get Consul Leader:
  - `curl -s http://127.0.0.1:8500/v1/status/leader | jq`
* Agent Info:
  - `curl -s http://127.0.0.1:8500/v1/agent/self | jq` <br>
