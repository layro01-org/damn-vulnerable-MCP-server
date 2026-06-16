# LINEAJE AI POLICY REPORT

**Run summary:** `violations_found` · violations=477 · remediation_actions=477 · elapsed=2166.5s

**Project Scanned:** `https://github.com/layro01-org/damn-vulnerable-MCP-server.git`

**Total Time:** 2166.5s

---

## Enforcement Summary

✅ **Remediated:** Use only LLMs from the organization's approved list. in `sse_server.py`

✅ **Remediated:** MCP server must validate and sanitize all input in `sse_server.py`

✅ **Remediated:** MCP clients must log all interactions with the MCP server in `sse_server.py`

✅ **Remediated:** Client must validate and sanitize any output from a MCP server in `sse_server.py`

✅ **Remediated:** MCP server must not interact directly with an LLM in `sse_server.py`

✅ **Remediated:** Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. in `sse_server.py`

✅ **Remediated:** Agents must log all interactions with an LLM in `sse_server.py`

✅ **Remediated:** The AI Model must validate and sanitize any input before processing. in `sse_server.py`

✅ **Remediated:** Sanitize and validate all input to the AI Model. in `sse_server.py`

✅ **Remediated:** Do not allow prompts that can execute malicious commands at runtime. in `sse_server.py`

✅ **Remediated:** Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. in `sse_server.py`

✅ **Remediated:** MCP client must authenticate MCP server in `sse_server.py`

*… and 465 more violation(s) — see **SECTION 3: Controls Enforced** below.*

**Summary:** 0 notified, 0 warned, 0 blocked, 12 remediated

---

### SECTION 1: AIBOM Discovery

#### AI Components

| AI Component Name | Type | Version | Source File |
|-------------------|------|---------|-------------|
| MCP Server · sse_server | MCP Server | 1.0.0 | sse_server.py |
| MCP Server · server_sse | MCP Server | 1.0.0 | challenges/easy/challenge1/server_sse.py |
| Challenge 1 - Basic Prompt Injection | MCP Server | 1.0.0 | challenges/easy/challenge1/server.py |
| MCP Server · server_sse | MCP Server | 1.0.0 | challenges/easy/challenge3/server_sse.py |
| Challenge 3 - Excessive Permission Scope | MCP Server | 1.0.0 | challenges/easy/challenge3/server.py |
| MCP Server · server_sse | MCP Server | 1.0.0 | challenges/easy/challenge2/server_sse.py |
| Challenge 2 - Tool Poisoning | MCP Server | 1.0.0 | challenges/easy/challenge2/server.py |
| MCP Server · server_sse | MCP Server | 1.0.0 | challenges/medium/challenge5/server_sse.py |
| Trusted Calculator Server | MCP Server | 1.0.0 | challenges/medium/challenge5/server.py |
| Enhanced Calculator Server | MCP Server | 1.0.0 | challenges/medium/challenge5/server.py |
| Challenge 5 - Tool Shadowing | MCP Server | 1.0.0 | challenges/medium/challenge5/server.py |
| MCP Server · server_sse | MCP Server | 1.0.0 | challenges/medium/challenge7/server_sse.py |
| Challenge 7 - Token Theft | MCP Server | 1.0.0 | challenges/medium/challenge7/server.py |
| MCP Server · server_sse | MCP Server | 1.0.0 | challenges/medium/challenge6/server_sse.py |
| Challenge 6 - Indirect Prompt Injection | MCP Server | 1.0.0 | challenges/medium/challenge6/server.py |
| MCP Server · server_sse | MCP Server | 1.0.0 | challenges/medium/challenge4/server_sse.py |
| Challenge 4 - Rug Pull Attack | MCP Server | 1.0.0 | challenges/medium/challenge4/server.py |
| MCP Server · server_sse | MCP Server | 1.0.0 | challenges/hard/challenge10/server_sse.py |
| Challenge 10 - Multi-Vector Attack | MCP Server | 1.0.0 | challenges/hard/challenge10/server.py |
| MCP Server · server_sse | MCP Server | 1.0.0 | challenges/hard/challenge9/server_sse.py |
| Challenge 9 - Remote Access Control | MCP Server | 1.0.0 | challenges/hard/challenge9/server.py |
| MCP Server · server_sse | MCP Server | 1.0.0 | challenges/hard/challenge8/server_sse.py |
| Challenge 8 - Malicious Code Execution | MCP Server | 1.0.0 | challenges/hard/challenge8/server.py |
| MCP Server · sse_server | MCP Server | 1.0.0 | common/sse_server.py |

### SECTION 2: Policy Violations

*Policies below are **only** those with at least one **`policy_violation=true`** result (one table row per distinct policy id, or per policy name if id is missing).*

| Policy Name | Description | Control Applied |
|-------------|-------------|-----------------|
| Use only LLMs from the organization's... | Use only LLMs from the organization's approved list. | Enforce Approved LLM. (Apply) |
| MCP server must validate and sanitize... | MCP server must validate and sanitize all input | Sanitize MCP Input (Apply) |
| MCP clients must log all interactions... | MCP clients must log all interactions with the MCP server | Log MCP Interaction (Apply) |
| Client must validate and sanitize any... | Client must validate and sanitize any output from a MCP server | Sanitize MCP Output (Apply) |
| MCP server must not interact directly... | MCP server must not interact directly with an LLM | Direct LLM Access by MCP (Apply) |
| Clear exit or termination criteria mu... | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | Missing Agent Exit Criteria (Apply) |
| Agents must log all interactions with... | Agents must log all interactions with an LLM | LLM Interaction Logging (Apply) |
| The AI Model must validate and saniti... | The AI Model must validate and sanitize any input before processing. | Sanitize LLM Input (Apply) |
| Sanitize and validate all input to th... | Sanitize and validate all input to the AI Model. | Sanitize LLM input (Apply) |
| Do not allow prompts that can execute... | Do not allow prompts that can execute malicious commands at runtime. | Block runtime command execution prompts. (Apply) |
| Enforce decision logging, audit trail... | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | Emit immutable, forensic-ready audit records for all AI decisions. (Apply) |
| MCP client must authenticate MCP server | MCP client must authenticate MCP server | Authenticate MCP Server (Apply) |
| MCP server must authenticate all clients | MCP server must authenticate all clients | Authenticate MCP Client (Apply) |
| Inter agent communication must be aut... | Inter agent communication must be authenticated. | Authenticate Agent Interactions (Apply) |
| LLM endpoints must require authentica... | LLM endpoints must require authentication | Authenticate inbound requests (Apply) |
| A user must authenticate before acces... | A user must authenticate before accessing the AI Agent. | Authenticate user before accessing AI Agent (Apply) |
| Restrict AI agents to an explicit too... | Restrict AI agents to an explicit tool allow list. | Allow only approved tools per task context. (Apply) |
| Enforce foundation model identity, ve... | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | Resolve all models from an approved registry with pinned versions. (Apply) |
| Enforce synthetic content provenance,... | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | Attach provenance, labels, and watermarks to all AI outputs. (Apply) |
| Do not allow malicious content via pr... | Do not allow malicious content via prompts included in source files. | Remove prompts with malicious and high risk system commands from source files (Apply) |
| Detect direct string interpolation of... | Detect direct string interpolation of untrusted input into LLM prompts | Enforce structural separation of untrusted input from LLM prompt templates (Apply) |
| Do not store secrets in code. | Do not store secrets in code. | Use Env Variables (Apply) |
| Mask PII on user interfaces | Mask PII on user interfaces | Mask PII on UI (Apply) |
| No file should contain any PII. | No file should contain any PII. | If a file contains PII, redact the PII (Apply) |
| Agents must not hold excessive extern... | Agents must not hold excessive external system credentials | Limit Excessive Credentials (Apply) |
| Maintain session token integrity with... | Maintain session token integrity with signing, verification, expiry, and binding. | Harden session token creation and validation. (Apply) |
| Do not allow critical or high vulnera... | Do not allow critical or high vulnerabilities in the code. | Fix code vulnerabilities (Apply) |
| Do not allow malicious content via hi... | Do not allow malicious content via hidden prompts | Replace suspicious prompt (Apply) |
| Enforce output data minimisation for... | Enforce output data minimisation for model, tool, and API responses. | Minimise and redact all outbound AI outputs. (Apply) |
| AI Agent must implement Human in the... | AI Agent must implement Human in the Loop (HITL) approval flow for risky operations like delete, purge, destroy | Implement HITL Approval flow (Apply) |
| Redact PII from uploaded files. | Redact PII from uploaded files. | Redact PII from uploaded files (Apply) |
| Uploaded files must not contain PII (... | Uploaded files must not contain PII (Singapore). | Redact PII (Singapore) from contents ofuploaded files (Apply) |
| Enforce URL allowlists for agent fetc... | Enforce URL allowlists for agent fetches, tools, and outbound HTTP. | Apply strict URL allowlists to agent HTTP. (Apply) |
| Detect and block agent privilege esca... | Detect and block agent privilege escalation attempts. | Stop privilege escalation in agent workflows. (Apply) |
| Enforce resource bounds, termination... | Enforce resource bounds, termination limits, and traceability for subagent spawning | Enforce lifecycle bounds and traceability for subagent spawning (Apply) |
| Do not log PII. | Do not log PII. | Mask PII in Logs (Apply) |
| Do not send PII to AI Models | Do not send PII to AI Models | Redact PII (Apply) |
| If PII data must be shared, it must b... | If PII data must be shared, it must be encrypted | Encrypt PII in Transit (Apply) |
| Do not allow malicious content via pr... | Do not allow malicious content via prompts included in uploaded files. | Remove suspicious prompts from uploaded files (Apply) |
| Do not allow malicious content via hi... | Do not allow malicious content via hidden prompts written in leetspeak. | Remove prompts in leetspeak (Apply) |
| Agent must validate, sanitize LLM out... | Agent must validate, sanitize LLM output including for presence of eval or any dynamic code execution primitive in LLM output. | LLM Interaction Logging (Apply) |

### SECTION 3: Controls Enforced

#### Controls enforced

| Control | Guardrail action | Policy Name | AI Component | Source File |
|---------|------------------|-------------|--------------|-------------|
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | MCP Server · sse_server | sse_server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | MCP Server · sse_server | sse_server.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | MCP Server · sse_server | sse_server.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | MCP Server · sse_server | sse_server.py |
| Direct LLM Access by MCP | Apply | MCP server must not interact directly with an LLM | MCP Server · sse_server | sse_server.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | MCP Server · sse_server | sse_server.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | MCP Server · sse_server | sse_server.py |
| Sanitize LLM Input | Apply | The AI Model must validate and sanitize any input before processing. | MCP Server · sse_server | sse_server.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | MCP Server · sse_server | sse_server.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | MCP Server · sse_server | sse_server.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | MCP Server · sse_server | sse_server.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | MCP Server · sse_server | sse_server.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | MCP Server · sse_server | sse_server.py |
| Authenticate Agent Interactions | Apply | Inter agent communication must be authenticated. | MCP Server · sse_server | sse_server.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | MCP Server · sse_server | sse_server.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | MCP Server · sse_server | sse_server.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | MCP Server · sse_server | sse_server.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | MCP Server · sse_server | sse_server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Remove prompts with malicious and high risk system commands from source files | Apply | Do not allow malicious content via prompts included in source files. | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Enforce structural separation of untrusted input from LLM prompt templates | Apply | Detect direct string interpolation of untrusted input into LLM prompts | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Use Env Variables | Apply | Do not store secrets in code. | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Mask PII on UI | Apply | Mask PII on user interfaces | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| If a file contains PII, redact the PII | Apply | No file should contain any PII. | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Limit Excessive Credentials | Apply | Agents must not hold excessive external system credentials | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Harden session token creation and validation. | Apply | Maintain session token integrity with signing, verification, expiry, and binding. | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | MCP Server · server_sse | challenges/easy/challenge1/server_sse.py |
| Replace suspicious prompt | Apply | Do not allow malicious content via hidden prompts | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Remove prompts with malicious and high risk system commands from source files | Apply | Do not allow malicious content via prompts included in source files. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Enforce structural separation of untrusted input from LLM prompt templates | Apply | Detect direct string interpolation of untrusted input into LLM prompts | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Use Env Variables | Apply | Do not store secrets in code. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Mask PII on UI | Apply | Mask PII on user interfaces | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| If a file contains PII, redact the PII | Apply | No file should contain any PII. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | Challenge 1 - Basic Prompt Injection | challenges/easy/challenge1/server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Sanitize LLM Input | Apply | The AI Model must validate and sanitize any input before processing. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Remove prompts with malicious and high risk system commands from source files | Apply | Do not allow malicious content via prompts included in source files. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Implement HITL Approval flow | Apply | AI Agent must implement Human in the Loop (HITL) approval flow for risky operations like delete, purge, destroy | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Redact PII from uploaded files | Apply | Redact PII from uploaded files. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Redact PII (Singapore) from contents ofuploaded files | Apply | Uploaded files must not contain PII (Singapore). | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| If a file contains PII, redact the PII | Apply | No file should contain any PII. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Authenticate Agent Interactions | Apply | Inter agent communication must be authenticated. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Apply strict URL allowlists to agent HTTP. | Apply | Enforce URL allowlists for agent fetches, tools, and outbound HTTP. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | MCP Server · server_sse | challenges/easy/challenge3/server_sse.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Sanitize LLM Input | Apply | The AI Model must validate and sanitize any input before processing. | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Use Env Variables | Apply | Do not store secrets in code. | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | Challenge 3 - Excessive Permission Scope | challenges/easy/challenge3/server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Remove prompts with malicious and high risk system commands from source files | Apply | Do not allow malicious content via prompts included in source files. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Implement HITL Approval flow | Apply | AI Agent must implement Human in the Loop (HITL) approval flow for risky operations like delete, purge, destroy | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Redact PII from uploaded files | Apply | Redact PII from uploaded files. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Redact PII (Singapore) from contents ofuploaded files | Apply | Uploaded files must not contain PII (Singapore). | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Authenticate Agent Interactions | Apply | Inter agent communication must be authenticated. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Enforce lifecycle bounds and traceability for subagent spawning | Apply | Enforce resource bounds, termination limits, and traceability for subagent spawning | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | MCP Server · server_sse | challenges/easy/challenge2/server_sse.py |
| Replace suspicious prompt | Apply | Do not allow malicious content via hidden prompts | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Direct LLM Access by MCP | Apply | MCP server must not interact directly with an LLM | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Remove prompts with malicious and high risk system commands from source files | Apply | Do not allow malicious content via prompts included in source files. | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | Challenge 2 - Tool Poisoning | challenges/easy/challenge2/server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Direct LLM Access by MCP | Apply | MCP server must not interact directly with an LLM | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Mask PII in Logs | Apply | Do not log PII. | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Redact PII | Apply | Do not send PII to AI Models | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Authenticate Agent Interactions | Apply | Inter agent communication must be authenticated. | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | MCP Server · server_sse | challenges/medium/challenge5/server_sse.py |
| Replace suspicious prompt | Apply | Do not allow malicious content via hidden prompts | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Remove prompts with malicious and high risk system commands from source files | Apply | Do not allow malicious content via prompts included in source files. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Implement HITL Approval flow | Apply | AI Agent must implement Human in the Loop (HITL) approval flow for risky operations like delete, purge, destroy | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Use Env Variables | Apply | Do not store secrets in code. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Encrypt PII in Transit | Apply | If PII data must be shared, it must be encrypted | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Redact PII | Apply | Do not send PII to AI Models | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Mask PII on UI | Apply | Mask PII on user interfaces | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| If a file contains PII, redact the PII | Apply | No file should contain any PII. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Limit Excessive Credentials | Apply | Agents must not hold excessive external system credentials | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | Trusted Calculator Server | challenges/medium/challenge5/server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Sanitize LLM Input | Apply | The AI Model must validate and sanitize any input before processing. | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Enforce structural separation of untrusted input from LLM prompt templates | Apply | Detect direct string interpolation of untrusted input into LLM prompts | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Use Env Variables | Apply | Do not store secrets in code. | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Harden session token creation and validation. | Apply | Maintain session token integrity with signing, verification, expiry, and binding. | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Enforce lifecycle bounds and traceability for subagent spawning | Apply | Enforce resource bounds, termination limits, and traceability for subagent spawning | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | MCP Server · server_sse | challenges/medium/challenge7/server_sse.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Sanitize LLM Input | Apply | The AI Model must validate and sanitize any input before processing. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Enforce structural separation of untrusted input from LLM prompt templates | Apply | Detect direct string interpolation of untrusted input into LLM prompts | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Use Env Variables | Apply | Do not store secrets in code. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Apply strict URL allowlists to agent HTTP. | Apply | Enforce URL allowlists for agent fetches, tools, and outbound HTTP. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Harden session token creation and validation. | Apply | Maintain session token integrity with signing, verification, expiry, and binding. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | Challenge 7 - Token Theft | challenges/medium/challenge7/server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Sanitize LLM Input | Apply | The AI Model must validate and sanitize any input before processing. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Remove suspicious prompts from uploaded files | Apply | Do not allow malicious content via prompts included in uploaded files. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Enforce structural separation of untrusted input from LLM prompt templates | Apply | Detect direct string interpolation of untrusted input into LLM prompts | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Redact PII from uploaded files | Apply | Redact PII from uploaded files. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Redact PII (Singapore) from contents ofuploaded files | Apply | Uploaded files must not contain PII (Singapore). | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| If a file contains PII, redact the PII | Apply | No file should contain any PII. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Authenticate Agent Interactions | Apply | Inter agent communication must be authenticated. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | MCP Server · server_sse | challenges/medium/challenge6/server_sse.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Remove suspicious prompts from uploaded files | Apply | Do not allow malicious content via prompts included in uploaded files. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Use Env Variables | Apply | Do not store secrets in code. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Mask PII on UI | Apply | Mask PII on user interfaces | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Redact PII from uploaded files | Apply | Redact PII from uploaded files. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Redact PII (Singapore) from contents ofuploaded files | Apply | Uploaded files must not contain PII (Singapore). | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| If a file contains PII, redact the PII | Apply | No file should contain any PII. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Authenticate Agent Interactions | Apply | Inter agent communication must be authenticated. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Limit Excessive Credentials | Apply | Agents must not hold excessive external system credentials | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | Challenge 6 - Indirect Prompt Injection | challenges/medium/challenge6/server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Implement HITL Approval flow | Apply | AI Agent must implement Human in the Loop (HITL) approval flow for risky operations like delete, purge, destroy | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | MCP Server · server_sse | challenges/medium/challenge4/server_sse.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Remove prompts with malicious and high risk system commands from source files | Apply | Do not allow malicious content via prompts included in source files. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Enforce structural separation of untrusted input from LLM prompt templates | Apply | Detect direct string interpolation of untrusted input into LLM prompts | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Implement HITL Approval flow | Apply | AI Agent must implement Human in the Loop (HITL) approval flow for risky operations like delete, purge, destroy | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Use Env Variables | Apply | Do not store secrets in code. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | Challenge 4 - Rug Pull Attack | challenges/medium/challenge4/server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Direct LLM Access by MCP | Apply | MCP server must not interact directly with an LLM | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Enforce structural separation of untrusted input from LLM prompt templates | Apply | Detect direct string interpolation of untrusted input into LLM prompts | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Redact PII from uploaded files | Apply | Redact PII from uploaded files. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Redact PII (Singapore) from contents ofuploaded files | Apply | Uploaded files must not contain PII (Singapore). | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| If a file contains PII, redact the PII | Apply | No file should contain any PII. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Authenticate Agent Interactions | Apply | Inter agent communication must be authenticated. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Apply strict URL allowlists to agent HTTP. | Apply | Enforce URL allowlists for agent fetches, tools, and outbound HTTP. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | MCP Server · server_sse | challenges/hard/challenge10/server_sse.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Remove prompts in leetspeak | Apply | Do not allow malicious content via hidden prompts written in leetspeak. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Remove suspicious prompts from uploaded files | Apply | Do not allow malicious content via prompts included in uploaded files. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Use Env Variables | Apply | Do not store secrets in code. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Encrypt PII in Transit | Apply | If PII data must be shared, it must be encrypted | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Mask PII on UI | Apply | Mask PII on user interfaces | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Redact PII from uploaded files | Apply | Redact PII from uploaded files. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Redact PII (Singapore) from contents ofuploaded files | Apply | Uploaded files must not contain PII (Singapore). | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| If a file contains PII, redact the PII | Apply | No file should contain any PII. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Authenticate Agent Interactions | Apply | Inter agent communication must be authenticated. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Limit Excessive Credentials | Apply | Agents must not hold excessive external system credentials | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Apply strict URL allowlists to agent HTTP. | Apply | Enforce URL allowlists for agent fetches, tools, and outbound HTTP. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Harden session token creation and validation. | Apply | Maintain session token integrity with signing, verification, expiry, and binding. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Enforce lifecycle bounds and traceability for subagent spawning | Apply | Enforce resource bounds, termination limits, and traceability for subagent spawning | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | Challenge 10 - Multi-Vector Attack | challenges/hard/challenge10/server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Direct LLM Access by MCP | Apply | MCP server must not interact directly with an LLM | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Sanitize LLM Input | Apply | The AI Model must validate and sanitize any input before processing. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Enforce structural separation of untrusted input from LLM prompt templates | Apply | Detect direct string interpolation of untrusted input into LLM prompts | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Implement HITL Approval flow | Apply | AI Agent must implement Human in the Loop (HITL) approval flow for risky operations like delete, purge, destroy | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Authenticate Agent Interactions | Apply | Inter agent communication must be authenticated. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Harden session token creation and validation. | Apply | Maintain session token integrity with signing, verification, expiry, and binding. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | MCP Server · server_sse | challenges/hard/challenge9/server_sse.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Remove prompts with malicious and high risk system commands from source files | Apply | Do not allow malicious content via prompts included in source files. | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Implement HITL Approval flow | Apply | AI Agent must implement Human in the Loop (HITL) approval flow for risky operations like delete, purge, destroy | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Encrypt PII in Transit | Apply | If PII data must be shared, it must be encrypted | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Mask PII in Logs | Apply | Do not log PII. | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Apply strict URL allowlists to agent HTTP. | Apply | Enforce URL allowlists for agent fetches, tools, and outbound HTTP. | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | Challenge 9 - Remote Access Control | challenges/hard/challenge9/server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| LLM Interaction Logging | Apply | Agent must validate, sanitize LLM output including for presence of eval or any dynamic code execution primitive in LLM output. | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Direct LLM Access by MCP | Apply | MCP server must not interact directly with an LLM | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | MCP Server · server_sse | challenges/hard/challenge8/server_sse.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Sanitize LLM Input | Apply | The AI Model must validate and sanitize any input before processing. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Remove suspicious prompts from uploaded files | Apply | Do not allow malicious content via prompts included in uploaded files. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Attach provenance, labels, and watermarks to all AI outputs. | Apply | Enforce synthetic content provenance, labeling, and watermarking for AI-generated outputs. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Enforce structural separation of untrusted input from LLM prompt templates | Apply | Detect direct string interpolation of untrusted input into LLM prompts | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Implement HITL Approval flow | Apply | AI Agent must implement Human in the Loop (HITL) approval flow for risky operations like delete, purge, destroy | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Use Env Variables | Apply | Do not store secrets in code. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Minimise and redact all outbound AI outputs. | Apply | Enforce output data minimisation for model, tool, and API responses. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Apply strict URL allowlists to agent HTTP. | Apply | Enforce URL allowlists for agent fetches, tools, and outbound HTTP. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Stop privilege escalation in agent workflows. | Apply | Detect and block agent privilege escalation attempts. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Enforce lifecycle bounds and traceability for subagent spawning | Apply | Enforce resource bounds, termination limits, and traceability for subagent spawning | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Fix code vulnerabilities | Apply | Do not allow critical or high vulnerabilities in the code. | Challenge 8 - Malicious Code Execution | challenges/hard/challenge8/server.py |
| Enforce Approved LLM. | Apply | Use only LLMs from the organization's approved list. | MCP Server · sse_server | common/sse_server.py |
| Sanitize MCP Input | Apply | MCP server must validate and sanitize all input | MCP Server · sse_server | common/sse_server.py |
| Log MCP Interaction | Apply | MCP clients must log all interactions with the MCP server | MCP Server · sse_server | common/sse_server.py |
| Sanitize MCP Output | Apply | Client must validate and sanitize any output from a MCP server | MCP Server · sse_server | common/sse_server.py |
| Direct LLM Access by MCP | Apply | MCP server must not interact directly with an LLM | MCP Server · sse_server | common/sse_server.py |
| Missing Agent Exit Criteria | Apply | Clear exit or termination criteria must exist for the agent to consider its task complete and stop executing. | MCP Server · sse_server | common/sse_server.py |
| LLM Interaction Logging | Apply | Agents must log all interactions with an LLM | MCP Server · sse_server | common/sse_server.py |
| Sanitize LLM input | Apply | Sanitize and validate all input to the AI Model. | MCP Server · sse_server | common/sse_server.py |
| Block runtime command execution prompts. | Apply | Do not allow prompts that can execute malicious commands at runtime. | MCP Server · sse_server | common/sse_server.py |
| Emit immutable, forensic-ready audit records for all AI decisions. | Apply | Enforce decision logging, audit trail, and forensic readiness for AI-driven actions. | MCP Server · sse_server | common/sse_server.py |
| Authenticate MCP Server | Apply | MCP client must authenticate MCP server | MCP Server · sse_server | common/sse_server.py |
| Authenticate MCP Client | Apply | MCP server must authenticate all clients | MCP Server · sse_server | common/sse_server.py |
| Authenticate inbound requests | Apply | LLM endpoints must require authentication | MCP Server · sse_server | common/sse_server.py |
| Authenticate user before accessing AI Agent | Apply | A user must authenticate before accessing the AI Agent. | MCP Server · sse_server | common/sse_server.py |
| Allow only approved tools per task context. | Apply | Restrict AI agents to an explicit tool allow list. | MCP Server · sse_server | common/sse_server.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | MCP Server · sse_server | common/sse_server.py |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | fastapi | requirements.txt |
| Resolve all models from an approved registry with pinned versions. | Apply | Enforce foundation model identity, version pinning, and approved model registry for all AI workloads. | dvmcp | pyproject.toml |

### AI Component Relationship Graph

```mermaid
graph TD
    mcp_server_1{{"🔧 MCP Server · sse_server<br/>sse_server.py"}}
    mcp_server_2{{"🔧 MCP Server · sse_server<br/>sse_server.py"}}
    mcp_server_3{{"🔧 MCP Server · sse_server<br/>sse_server.py"}}
    mcp_server_4{{"🔧 MCP Server · sse_server<br/>sse_server.py"}}
    package_5["📦 fastapi<br/>requirements.txt"]
    package_6["📦 uvicorn<br/>requirements.txt"]
    package_7["📦 httpx<br/>requirements.txt"]
    package_8["📦 mcp<br/>requirements.txt"]
    package_9["📦 starlette<br/>requirements.txt"]
    package_10["📦 dvmcp<br/>pyproject.toml"]
    mcp_server_11{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_12{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_13{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_14{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_15{{"🔧 Challenge 1 - Basic Prompt Injection<br/>server.py"}}
    mcp_server_16{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_17{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_18{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_19{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_20{{"🔧 Challenge 3 - Excessive Permission Scope<br/>server.py"}}
    mcp_server_21{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_22{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_23{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_24{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_25{{"🔧 Challenge 2 - Tool Poisoning<br/>server.py"}}
    mcp_server_26{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_27{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_28{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_29{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_30{{"🔧 Trusted Calculator Server<br/>server.py"}}
    mcp_server_31{{"🔧 Enhanced Calculator Server<br/>server.py"}}
    mcp_server_32{{"🔧 Challenge 5 - Tool Shadowing<br/>server.py"}}
    mcp_server_33{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_34{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_35{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_36{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_37{{"🔧 Challenge 7 - Token Theft<br/>server.py"}}
    mcp_server_38{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_39{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_40{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_41{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_42{{"🔧 Challenge 6 - Indirect Prompt Injection<br/>server.py"}}
    mcp_server_43{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_44{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_45{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_46{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_47{{"🔧 Challenge 4 - Rug Pull Attack<br/>server.py"}}
    mcp_server_48{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_49{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_50{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_51{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_52{{"🔧 Challenge 10 - Multi-Vector Attack<br/>server.py"}}
    mcp_server_53{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_54{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_55{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_56{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_57{{"🔧 Challenge 9 - Remote Access Control<br/>server.py"}}
    mcp_server_58{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_59{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_60{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_61{{"🔧 MCP Server · server_sse<br/>server_sse.py"}}
    mcp_server_62{{"🔧 Challenge 8 - Malicious Code Execution<br/>server.py"}}
    mcp_server_63{{"🔧 MCP Server · sse_server<br/>sse_server.py"}}
    mcp_server_64{{"🔧 MCP Server · sse_server<br/>sse_server.py"}}
    mcp_server_65{{"🔧 MCP Server · sse_server<br/>sse_server.py"}}
    mcp_server_66{{"🔧 MCP Server · sse_server<br/>sse_server.py"}}

    classDef agent fill:#4CAF50,stroke:#333,color:#fff
    classDef model fill:#2196F3,stroke:#333,color:#fff
    classDef mcp fill:#FF9800,stroke:#333,color:#fff
    classDef rag fill:#9C27B0,stroke:#333,color:#fff
    classDef skill fill:#00BCD4,stroke:#333,color:#fff
    classDef agentconfig fill:#795548,stroke:#333,color:#fff
    class mcp_server_1 mcp
    class mcp_server_2 mcp
    class mcp_server_3 mcp
    class mcp_server_4 mcp
    class package_5 package
    class package_6 package
    class package_7 package
    class package_8 package
    class package_9 package
    class package_10 package
    class mcp_server_11 mcp
    class mcp_server_12 mcp
    class mcp_server_13 mcp
    class mcp_server_14 mcp
    class mcp_server_15 mcp
    class mcp_server_16 mcp
    class mcp_server_17 mcp
    class mcp_server_18 mcp
    class mcp_server_19 mcp
    class mcp_server_20 mcp
    class mcp_server_21 mcp
    class mcp_server_22 mcp
    class mcp_server_23 mcp
    class mcp_server_24 mcp
    class mcp_server_25 mcp
    class mcp_server_26 mcp
    class mcp_server_27 mcp
    class mcp_server_28 mcp
    class mcp_server_29 mcp
    class mcp_server_30 mcp
    class mcp_server_31 mcp
    class mcp_server_32 mcp
    class mcp_server_33 mcp
    class mcp_server_34 mcp
    class mcp_server_35 mcp
    class mcp_server_36 mcp
    class mcp_server_37 mcp
    class mcp_server_38 mcp
    class mcp_server_39 mcp
    class mcp_server_40 mcp
    class mcp_server_41 mcp
    class mcp_server_42 mcp
    class mcp_server_43 mcp
    class mcp_server_44 mcp
    class mcp_server_45 mcp
    class mcp_server_46 mcp
    class mcp_server_47 mcp
    class mcp_server_48 mcp
    class mcp_server_49 mcp
    class mcp_server_50 mcp
    class mcp_server_51 mcp
    class mcp_server_52 mcp
    class mcp_server_53 mcp
    class mcp_server_54 mcp
    class mcp_server_55 mcp
    class mcp_server_56 mcp
    class mcp_server_57 mcp
    class mcp_server_58 mcp
    class mcp_server_59 mcp
    class mcp_server_60 mcp
    class mcp_server_61 mcp
    class mcp_server_62 mcp
    class mcp_server_63 mcp
    class mcp_server_64 mcp
    class mcp_server_65 mcp
    class mcp_server_66 mcp
```

### Phase Timing

| Phase | Time |
|-------|------|
| policy_loading | 1.6s |
| discovery | 1.1s |
| tool_prefetch | 100.8s |
| evaluation | 577.9s |
| remediation | 1485.0s |
| **Total** | **2166.5s** |
