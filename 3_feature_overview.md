# Feature Overview

- **Agent** - what you create to interact with in Snowflake Intelligence. Created via Snowsight, these are also possible to create programatically via SQL. In order to show up in Snowflake Intelligence, they must exist in the `snowflake_intelligence.agents` schema.

```sql
CREATE AGENT SNOWFLAKE_INTELLIGENCE.AGENTS.SNOWFLAKE_DOCS_AGENT
WITH PROFILE='{ "display_name": "Snowflake Docs Agent" }'
    COMMENT=$$ This is an agent that can answer questions about Snowflake documentation. It uses the Snowflake documentation marketplace knowledge extension. $$
FROM SPECIFICATION $$
{
    "models": { "orchestration": "auto" },
    "instructions": {
        "response": "",
        "orchestration": "",
        "sample_questions": [
            { "question": "How do I create an Iceberg table?" }
        ]
    },
    "tools": [
        {
            "tool_spec": {
            "name": "Snowflake_Documentation",
            "type": "cortex_search"
            }
        },
        {
            "tool_spec": {
            "description": "Tool description...",
            "name": "My_Semantic_View",
            "type": "cortex_analyst_text_to_sql"
            }
        }
    ],
    "tool_resources": {
        "Snowflake_Documentation": {
            "id_column": "URL",
            "max_results": 10,
            "name": "SNOWFLAKE_DOCUMENTATION.PUBLIC.DOCUMENTATION"
        },
        "My_Semantic_View": {
            "semantic_view": "SNOWFLAKE_INTELLIGENCE_DEMO.PRODUCT_INFO.AURA_PRODUCT_INFO"
        }
        }
}
$$;
```

*Response Instructions* - Used to guide the final generation of an agent, not how an agent will get to the answer
*Planning (Orchestration) Instructions*  - Used to guide how an agent will get to the answer, including which tools to use, or general guides on which tools to call, when to ask for clarification, etc.

