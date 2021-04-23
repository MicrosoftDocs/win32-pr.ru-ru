---
title: Нормализация текста для модулей преобразования текста в речь
description: Нормализация текста для модулей преобразования текста в речь
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7bda7cb8041e31ef8e741df4d3f5d807610f1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700553"
---
# <a name="text-to-speech-engines-text-normalization"></a><span data-ttu-id="5ca23-103">Нормализация текста для модулей преобразования текста в речь</span><span class="sxs-lookup"><span data-stu-id="5ca23-103">Text-to-Speech Engines Text Normalization</span></span>

<span data-ttu-id="5ca23-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5ca23-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="5ca23-105">Нормализация — это процесс идентификации чисел, сокращений, аббревиатур и идиоматикс, а также преобразования их в полный текст по мере необходимости, обычно на основе контекста предложения.</span><span class="sxs-lookup"><span data-stu-id="5ca23-105">Normalization is the process of identifying numbers, abbreviations, acronyms and idiomatics and transforming them into full text as needed, usually based on the context of the sentence.</span></span>

<span data-ttu-id="5ca23-106">Например, с помощью обработчика "L&H Трувоице американский английский TTS", предложение:</span><span class="sxs-lookup"><span data-stu-id="5ca23-106">For example, using the L&H TruVoice American English TTS Engine, the sentence:</span></span>

<span data-ttu-id="5ca23-107">Короля Георгия, умер, 1952.</span><span class="sxs-lookup"><span data-stu-id="5ca23-107">King George VI of England died on Feb 6, 1952.</span></span>

<span data-ttu-id="5ca23-108">будет считаться в **нормальном контексте** как:</span><span class="sxs-lookup"><span data-stu-id="5ca23-108">will be read under **normal context** as:</span></span>

   <span data-ttu-id="5ca23-109">Короля 19 52 в 1 февраля, умер.</span><span class="sxs-lookup"><span data-stu-id="5ca23-109">King George V I of England, died on February six, nineteen fifty-two.</span></span>

<span data-ttu-id="5ca23-110">Но в **контексте сообщения электронной почты** она будет считаться:</span><span class="sxs-lookup"><span data-stu-id="5ca23-110">But under **E-mail context**, it will be read as:</span></span>

   <span data-ttu-id="5ca23-111">Короля Георгия — шестая часть Англия, умер в шестой 19 52 февраля.</span><span class="sxs-lookup"><span data-stu-id="5ca23-111">King George the sixth of England, died on February sixth, nineteen fifty-two.</span></span>

<span data-ttu-id="5ca23-112">Сведения об использовании **контекстного** речевого тега см. в документации по программированию агента [речевого вывода для агента Microsoft Agent](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="5ca23-112">Information about using the **Context** speech tag can be found in the Agent programming documentation [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




