# Camunda n8n Bridge

Connect your Camunda 7 BPMN processes to n8n workflows. Unlock 400+ integrations for your existing Camunda 7.

## What is this?

A simple Java delegate that bridges Camunda 7 service tasks to n8n webhooks. Your Camunda 7 process calls the delegate, the delegate calls n8n, n8n does the work.

## Installation

Download the latest JAR from [Releases](https://github.com/AlainJaques22/camunda-n8n-bridge/releases) and add it to your Camunda 7 `lib/` folder.

## Usage

In your BPMN service task, set:
- **Implementation:** Java Class
- **Java Class:** `io.catalyst.bridge.CatalystBridge`

Configure input parameters:
- `webhookUrl` - Your n8n webhook URL
- `payload` - JSON payload with `${variable}` substitution
- `timeout` - Request timeout in seconds (default: 30)

## Bidirectional Integration

This bridge handles **Camunda → n8n** communication.

For **n8n → Camunda** (starting processes, completing tasks from n8n), see the companion project: [n8n-nodes-camunda7](https://github.com/AlainJaques22/n8n-nodes-camunda7)

## License

MIT — Use it however you want.

## Part of Catalyst

This bridge is the open-source core of [Catalyst](https://catalyst-connector.com), which provides pre-built, validated connectors for Camunda 7.
