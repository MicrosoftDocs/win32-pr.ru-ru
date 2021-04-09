---
title: Строки и сообщения команд MCI
description: Строки и сообщения команд MCI
ms.assetid: eb60c96b-e89e-4673-a8e0-98fabe4af7ca
keywords:
- Строки команд MCI, сведения
- Сообщения команды MCI, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a317442280b8fb4c7afe7832205b1c7128513
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890652"
---
# <a name="mci-command-strings-and-messages"></a><span data-ttu-id="2bd6b-105">Строки и сообщения команд MCI</span><span class="sxs-lookup"><span data-stu-id="2bd6b-105">MCI Command Strings and Messages</span></span>

<span data-ttu-id="2bd6b-106">MCI поддерживает [Командные строки](command-strings.md) и [Командные сообщения](command-messages.md).</span><span class="sxs-lookup"><span data-stu-id="2bd6b-106">MCI supports [Command Strings](command-strings.md) and [Command Messages](command-messages.md).</span></span> <span data-ttu-id="2bd6b-107">В приложении MCI можно использовать как строки, так и сообщения.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-107">You can use either strings or messages, or both, in your MCI application.</span></span>

-   <span data-ttu-id="2bd6b-108">*Интерфейс командных сообщений* состоит из констант и структур.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-108">The *command-message interface* consists of constants and structures.</span></span> <span data-ttu-id="2bd6b-109">Используйте функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) для отправки сообщений на устройство MCI.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-109">Use the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send messages to an MCI device.</span></span>
-   <span data-ttu-id="2bd6b-110">*Интерфейс командной строки* предоставляет текстовую версию командных сообщений.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-110">The *command-string interface* provides a textual version of the command messages.</span></span> <span data-ttu-id="2bd6b-111">Используйте функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) для отправки строк на устройство MCI.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-111">Use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function to send strings to an MCI device.</span></span> <span data-ttu-id="2bd6b-112">Строки команд дублируют функциональность командных сообщений.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-112">Command strings duplicate the functionality of the command messages.</span></span> <span data-ttu-id="2bd6b-113">Операционная система преобразует строки команд в командные сообщения перед их отправкой драйверу MCI для обработки.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-113">The operating system converts the command strings to command messages before sending them to the MCI driver for processing.</span></span>

<span data-ttu-id="2bd6b-114">Командные сообщения, которые получают информацию, делают это в виде структур, которые легко интерпретировать в приложении на языке C.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-114">The command messages that retrieve information do so in the form of structures, which are easy to interpret in a C application.</span></span> <span data-ttu-id="2bd6b-115">Эти структуры могут содержать сведения о множестве различных аспектов устройства.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-115">These structures can contain information on many different aspects of a device.</span></span> <span data-ttu-id="2bd6b-116">Командные строки, которые извлекают сведения, делают это в виде строк и могут получить только одну строку за раз.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-116">The command strings that retrieve information do so in the form of strings, and can only retrieve one string at a time.</span></span> <span data-ttu-id="2bd6b-117">Приложение должно проанализировать или протестировать каждую строку, чтобы интерпретировать ее.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-117">Your application must parse or test each string to interpret it.</span></span> <span data-ttu-id="2bd6b-118">Может оказаться, что командные сообщения проще в использовании, чем командные строки в некоторых случаях, но командные строки легко запомнить и реализовать.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-118">You might find that the command messages are easier to use than the command strings in some cases, but the command strings are easy to remember and implement.</span></span> <span data-ttu-id="2bd6b-119">Некоторые приложения MCI используют строки команд, если возвращаемое значение не будет использоваться (за исключением проверки успешности) и командных сообщений при извлечении данных с устройства.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-119">Some MCI applications use command strings when the return value will not be used (other than to verify success) and command messages when retrieving information from the device.</span></span>

<span data-ttu-id="2bd6b-120">При обсуждении команд в этом обзоре используется строковая форма команды, за которой следует форма сообщения в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="2bd6b-120">When commands are discussed, this overview uses the string form of the command followed by the message form in parentheses.</span></span>

 

 