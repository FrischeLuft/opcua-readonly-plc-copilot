opcua-readonly-plc-copilot

What it does
A read-only PLC copilot that explains current machine state based on real tag/alarm data via OPC UA. It answers engineer questions with facts → interpretation → next steps.

Typical use cases

* “Why is the line stopped?” → active alarms + key tags + recommended checks

* “What changed in the last 10 minutes?” → event summary

* Operator shift handover summaries

Architecture (high level)

* Data: OPC UA server (demo uses a simulator)

* Adapter: read-only tag/alarms access (JSON tools)

* Copilot: chat API that calls tools and formats responses

* Audit: logs of questions, tool calls, and outputs

Demo (local)

* Runs against a simulated OPC UA endpoint (no real PLC required).

* Demonstrates safe operation: read-only tools + rate limits + logging.

Deliverables (for a client pilot)

* OPC UA adapter and tag model mapping

* Read-only copilot interface (chat/API)

* Logging/audit trail for traceability

* Pilot documentation + safety constraints

Safety / limitations

* Strictly read-only by design.

* Any write actions (if ever required) must go through a separate gated control layer (whitelist, validation, approvals).

Contact
Freelance / pilot projects: Industrial Automation + AI + n8n workflows
(Email: igor.pokhotelov@outlook.de)
