```md
---
title: OpenAI node documentation
description: Learn how to use the OpenAI node in n8n. Follow the technical documentation to integrate the OpenAI node into your workflows.
contentType: [integration, reference]
priority: critical
search:
    boost: 3
---

# OpenAI node

Use the OpenAI node to build AI-powered workflows in n8n, including chat assistants, document analysis, image generation, transcription, and tool-enabled AI agents.

On this page, you'll find a list of operations the OpenAI node supports and links to more resources.

/// note | Previous node versions
The OpenAI node replaces the OpenAI assistant node from version 1.29.0 onward.

n8n version 1.117.0 introduces V2 of the OpenAI node, which supports the OpenAI Responses API and removes support for the to-be-deprecated Assistants API.
///

/// note | Chat Completions vs Responses API
OpenAI currently supports both the Chat Completions API and the newer Responses API.

Use:
- **Generate a Chat Completion** for compatibility with existing chat-based workflows.
- **Generate a Model Response** for newer OpenAI models and advanced features such as tool calling, structured outputs, and multimodal inputs.
///

/// note | Credentials
Refer to [OpenAI credentials](/integrations/builtin/credentials/openai.md) for guidance on setting up authentication.
///

## Operations

- **Text**
	- [**Generate a Chat Completion**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/text-operations.md#generate-a-chat-completion)
	- [**Generate a Model Response**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/text-operations.md#generate-a-model-response)
	- [**Classify Text for Violations**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/text-operations.md#classify-text-for-violations)

- **Image**
	- [**Analyze Image**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/image-operations.md#analyze-image)
	- [**Generate an Image**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/image-operations.md#generate-an-image)
	- [**Edit an Image**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/image-operations.md#edit-an-image)

- **Audio**
	- [**Generate Audio**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/audio-operations.md#generate-audio)
	- [**Transcribe a Recording**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/audio-operations.md#transcribe-a-recording)
	- [**Translate a Recording**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/audio-operations.md#translate-a-recording)

- **File**
	- [**Delete a File**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/file-operations.md#delete-a-file)
	- [**List Files**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/file-operations.md#list-files)
	- [**Upload a File**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/file-operations.md#upload-a-file)

- **Video**
	- [**Generate a Video**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/video-operations.md#generate-video)

- **Conversation**
	- [**Create a Conversation**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/conversation-operations.md#create-a-conversation)
	- [**Get a Conversation**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/conversation-operations.md#get-a-conversation)
	- [**Update a Conversation**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/conversation-operations.md#update-a-conversation)
	- [**Remove a Conversation**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/conversation-operations.md#remove-a-conversation)

## Choosing the right operation

Use:
- **Generate a Chat Completion** for conversational text generation and compatibility with existing workflows.
- **Generate a Model Response** for modern OpenAI workflows that use tools, structured outputs, or multimodal inputs.
- **Analyze Image** for image understanding and vision tasks.
- **Generate Audio** for text-to-speech workflows.
- **Transcribe a Recording** for speech-to-text automation.

## Templates and examples

<!-- see https://www.notion.so/n8n/Pull-in-templates-for-the-integrations-pages-37c716837b804d30a33b47475f6e3780 -->
[[ templatesWidget(page.title, 'openai') ]]

## Related resources

Refer to [OpenAI's API documentation](https://platform.openai.com/docs) for more information about the service.

Refer to [Handling rate limits](/integrations/builtin/rate-limits.md) for help dealing with API rate limits.

--8<-- "_snippets/integrations/builtin/app-nodes/operation-not-supported.md"

## Using tools with OpenAI

Some operations allow you to connect tools. [Tools](/advanced-ai/examples/understand-tools.md) act like addons that your AI can use to access external systems, APIs, or additional context.

Examples of tools include:
- HTTP Request nodes for external APIs
- Database nodes for retrieving records
- Vector stores for document retrieval
- Calculator tools for mathematical operations

Select the **Tools** connector to browse the available tools and add them.

Once you add a tool connection, the OpenAI node becomes a [root node](/glossary.md#root-node-n8n), allowing it to form a [cluster node](/glossary.md#cluster-node-n8n) with the connected tools as [sub-nodes](/glossary.md#sub-node-n8n).

See [Node types](/integrations/builtin/node-types.md#cluster-nodes) for more information on cluster nodes and root nodes.

### Operations that support tool connectors

- **Text**
	- [**Generate a Chat Completion**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/text-operations.md#generate-a-chat-completion)
	- [**Generate a Model Response**](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/text-operations.md#generate-a-model-response)

## Common issues

Common issues include:
- rate limit errors
- authentication failures
- invalid JSON outputs
- token limit errors
- tool execution failures

For troubleshooting steps and suggested solutions, refer to [Common issues](/integrations/builtin/app-nodes/n8n-nodes-langchain.openai/common-issues.md).
```
