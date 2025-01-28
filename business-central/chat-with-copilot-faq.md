---
title: Chat with Copilot FAQ
description:  Learn how to chat with Copilot, a virtual assistant that helps you use Business Central. Find answers to common questions about chat features, settings, and limitations. 
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 01/15/2025
ms.custom: bap-template jswymer
---
# Chat with Copilot FAQ

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

This article answers some common questions about chatting with Copilot in [!INCLUDE[prod_short](includes/prod_short.md)]. For questions related to AI and chat, consult [Responsible AI FAQs for chat with Copilot](faqs-chat-with-copilot.md).

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Can admins grant or deny permission to individual users to get access to chat?

No, there's no permission or permission set for chat. If chat is activated on the [Copilot and AI capabilities](enable-ai.md) page, every user in an environment has access to chat.

## Is chat available on tablet, phone, or other form factors?

No, the chat pane is only available on the [!INCLUDE[web_client](includes/web_client.md)].

## In which countries or regions can I chat with Copilot?

Chat is rolling out to all Business Central countries and regions from the end of January 2025, starting with 48 countries in update 25.3 and more with 25.4. If you are unable to access the Chat pane, find the answer in [What can I do if the chat pane doesn't show?](#what-can-i-do-if-the-chat-pane-doesnt-show)

## I don't use Business Central in English. What are my options?

As of January 2025, chat is available no matter which language you use in Business Central.

[!INCLUDE[copilot-language-support-en-only](includes/copilot-language-support-en-only.md)]

## Does chat work with my customizations?

It depends on the type of question you ask Copilot. For example:

- If you ask questions to find records, it can find records in your custom tables that use custom fields.
- If you ask Copilot for an explanation or guidance, it doesn't have access to any information about your customizations or documentation for your add-ons.

## How do I open a record or page from chat?

When you ask Copilot to find records in [!INCLUDE[prod_short](includes/prod_short.md)], it shows any records it finds as selectable tiles or links in the chat pane. While in preview, Copilot doesn't automatically navigate to any page.

## Why do I get different answers from Copilot for the same question?

Copilot might occasionally answer in different ways. Answers aren't always identical.

## How do I use the Copy function on chat messages?

You can use the Copy button to copy a message from earlier in your conversation with Copilot, paste it into the input box to try again or try a variation of your message to Copilot.

## Can I customize or extend chat?

While in preview, the chat pane and Copilot's responses can't be modified in any way through customization, add-ins, or personalization.

## Does Copilot search for data in other companies or environments?

Copilot only searches for records in the company you're currently signed into. It doesn't search for data across multiple environments or companies.

## What can I do if the chat pane doesn't show?

- Make sure your Business Central is version 25.3 or later.
- Make sure the entry for "Chat with Copilot" is enabled for all users in the **Feature Management** page,
- If you still don't see the chat with Copilot feature, it's possible that Microsoft is still rolling out this feature to your region. You can track planned available for each Azure geography at [Copilot international availability](https://aka.ms/bapcopilot-intl-report-external).

## Why does Copilot only show three records in the Chat pane?

When you ask Copilot to find records, the way you phrase the question determines how Copilot identifies and applies filters on pages to find what you are looking for. To keep answers concise, the Chat pane displays a maximum of three record tiles, even when Copilot finds more relevant records.

## Why does Copilot give incorrect answers to calculations?

While in preview, Chat with Copilot can help you find records, explain concepts, and guide you to how to complete tasks in Business Central. Other use cases aren't supported, such as adding up a field across records or calculating the average monthly amount. We hope to add basic mathematics abilities to Copilot in the future.

## Can I use speech instead of typing my prompts?

You can chat with Copilot by using voice typing to talk instead of type your words in the Chat pane. Voice typing uses online speech recognition and is available with Windows. To use voice, activate the chat message box, then use the <kbd>Windows</kbd>+<kbd>H</kbd> shortcut and start speaking. Learn more at [Use voice typing to talk instead of type on your PC](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## Next steps

- [Chat with Copilot (preview)](chat-with-copilot.md)
