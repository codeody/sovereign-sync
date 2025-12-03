# PROJECT SOVEREIGN SYNC: PHASE 1 DIRECTIVES
**STATUS:** ACTIVE
**OBJECTIVE:** Achieve a functional, real-time group chat MVP for fleet-wide communication.

---

### **TO: THE ENGINE ROOM (Auxilio, Veritas1, B4_Pre)**
*   **[B4_Pre]:** Take lead on creating the initial Docker Compose configuration (`docker-compose.yml`) for the project. Define the core services: the main web server, the collector, and the vector database based on the forked AnythingLLM architecture. Ensure it can build and run locally.
*   **[Veritas1]:** Begin mapping the database schema required for the GangSh-t chat. Define the tables for `users`, `messages`, `channels`, and `threads`. Prepare the initial SQL migration script.
*   **[Auxilio]:** Architect the high-level API contract between the frontend and backend. Define the WebSocket event names and payload structures (e.g., `message:create`, `user:typing`, `channel:join`) that will be used for real-time communication.

### **TO: THE BRIDGE (SwitchTrigger, Oxye, Prefix, Qu4dCanon)**
*   **[SwitchTrigger]:** Take lead on setting up the RabbitMQ service within the Docker Compose file provided by Pre. Define the initial exchange (`fleet_chat_exchange`) and queues (`chat_messages_q`, `system_events_q`) for the chat system.
*   **[Oxye]:** Begin research and documentation on the existing AnythingLLM backend API. Trace the data flow for a standard chat query to understand how we can hook into it for our RAG-in-chat feature in Phase 2.
*   **[Prefix, Qu4dCanon]:** Work together to research and prototype a basic Node.js WebSocket server that can connect to SwitchTrigger's RabbitMQ instance. Your goal is to create a simple proof-of-concept that can receive a message from RabbitMQ and broadcast it to a connected WebSocket client.

### **TO: THE DECK (W3bSlinger, Elec7ron, Over5layer, Feight)**
*   **[W3bSlinger]:** Take lead on creating a new, standalone UI component within the frontend codebase for the "GangSh-t" chat. For now, focus purely on functionality: an input box, a message display area, and a user list. Use placeholder data. Do not focus on aesthetics yet.
*   **[Over5layer, Feight]:** Begin assembling a "mood board" and style guide for the Sovereign Sync aesthetic. Collect ASCII art, color palettes (#7209B7, #00B4D8, #FFB703), fonts, and UI concepts that align with the Space Gang brand.
*   **[Elec7ron]:** Research how the current AnythingLLM frontend displays system information. Identify the components we can repurpose or will need to build for displaying real-time fleet status indicators in the future.

---
**ALL CREWS:** Clone the repository. Read these directives. Begin execution. Communicate progress via commits.
**SIG:** CAPTAIN HERU ODYSSEY | VIA AUXILIO
