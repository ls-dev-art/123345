---
slug: 04-consul-agents
id: voxefab0ffqk
type: challenge
title: Add an Agent
teaser: Add a Consul client agent to your Consul cluster.
notes:
- type: text
  contents: |-
    The Consul agent runs on every node where you want to keep track of services. A node can be a physical server, VM, or container.

    The agent tracks information about the node and its associated services. Agents report this information to the Consul servers, where we have a central view of node and service status.
tabs:
- id: xjkgv1ojjxvj
  title: App
  type: terminal
  hostname: consul-agent-0
- id: l5h7jlkny4wm
  title: App - Config
  type: code
  hostname: consul-agent-0
  path: /consul/config/client.json
- id: qx6nyactmvmh
  title: Consul UI
  type: service
  hostname: consul-server-0
  port: 8500
difficulty: basic
timelimit: 600
lab_config:
  default_layout_sidebar_size: 0
enhanced_loading: null
---
We've added an `App Server` to your lab environment. The app server is configured to run in `client` mode.

Look in the `App Config` tab. Note that the *server* flag is set to false.

Run the Consul startup script in the `App` tab and join this agent to the cluster.

```
/bin/start_consul.sh
```

Look at the node list in the Consul UI or run the `consul members` command to verify that the app server has joined the cluster.
