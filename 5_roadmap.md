# Roadmap

Here’s a glimpse at the current high-level backlog for Snowflake Intelligence. The list here may shift and evolve heavily based on your feedback, but may be useful to know what may be lighting up soon:

**Call a custom action** \- Rolling out now \- can call a procedure in your Snowflake account to pull in data from somewhere else (e.g. get weather), take an action (e.g. create a Salesforce record / send an email), or whatever you write Python code to do

**Web Search** \- \~July / August

**Make it easier to create semantic models \-** PrPr now, more rolling out over coming weeks. E.g. “Import from Tableau dashboard”, “Learn from internal documentation about your data”, “Look at your query history”, “Auto-tune my model to be able to accurately answer these 20 eval questions”

**Agent creation experience \- full** \- a larger experience in Snowsight to define knowledge sources, instructions, actions, and hae a playground to test agents. Would include UI to invite other users \- \~**July 10**

**Save charts or outputs for frequent lookup / refresh** \- \~Aug

General chart improvements (more chart types, look+feel) \- \~Aug

Call an agent via MCP \- \~Aug  
Add MCP server as a tool \- \~Sept

Ability to define a specific “workflow” for an agent to follow (e.g. to generate a health report for my customer, first do this, then do this, then do that) \- \~Sept

Teams integration (\~Q4)  
Slack integration (\~Q4)

**No ETA, but directional things we are chewing on:**

- Support Agent 2 Agent, so you can seamlessly have your Snowflake Intelligence Agent call or communicate with other agents (\~Q4)  
- Out of the box eval support \- let users define a set of questions they want to ensure the agent can answer and we will periodically check to make sure it can answer  
- Integrate forecasting and ML models into Agent responses (out of the box or custom models)  
- Send periodic digests or reports on data that you care about (e.g. here’s something interesting that’s happened in data that you care about)  
- Add Streamlit or custom UI apps to [ai.snowflake.com](http://ai.snowflake.com)  
- The ability for an agent to turn a conversation into a more shareable / re-usable custom app / streamlit