---
title: Поддержка всплывающих окон Word
description: Поддержка всплывающих окон Word
ms.assetid: deac032f-0480-4a0d-bc69-e26f12666bbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78316c509ece6fc8f9b0cefd50b1564a50697a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253036"
---
# <a name="word-balloon-support"></a><span data-ttu-id="36f5e-103">Поддержка всплывающих окон Word</span><span class="sxs-lookup"><span data-stu-id="36f5e-103">Word Balloon Support</span></span>

<span data-ttu-id="36f5e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="36f5e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="36f5e-105">Речевое вывод может также отображаться в виде текстового вывода в виде всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="36f5e-105">Spoken output can also appear as textual output in the form of a cartoon word balloon.</span></span> <span data-ttu-id="36f5e-106">Это можно использовать для дополнения выходного текста символа или в качестве альтернативы выходным данным при использовании метода [**говорите**](speak-method.md) .</span><span class="sxs-lookup"><span data-stu-id="36f5e-106">This can be used to supplement the spoken output of a character or as an alternative to audio output when you use the [**Speak**](speak-method.md) method.</span></span>

![всплывающее главное слово Yes](images/f3ballon.gif)

<span data-ttu-id="36f5e-108">Можно также использовать всплывающую подсказку, чтобы сообщить, что символ «думает» с помощью метода [**обработки**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="36f5e-108">You can also use a word balloon to communicate what a character is "thinking" using the [**Think**](think-method.md) method.</span></span> <span data-ttu-id="36f5e-109">Здесь отображается текст, который вы передаете по-прежнему «мысль».</span><span class="sxs-lookup"><span data-stu-id="36f5e-109">This displays the text you supply in a still "thought" balloon.</span></span> <span data-ttu-id="36f5e-110">Метод **обработки** также отличается от метода [**говорите**](speak-method.md) тем, что он не создает звуковых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="36f5e-110">The **Think** method also differs from the [**Speak**](speak-method.md) method in that it produces no audio output.</span></span>

<span data-ttu-id="36f5e-111">В тексте Word поддерживаются только подписанные сообщения, а не вводимые пользователем данные.</span><span class="sxs-lookup"><span data-stu-id="36f5e-111">Word balloons support only captioned communication from the character, not user input.</span></span> <span data-ttu-id="36f5e-112">Таким образом, всплывающее сообщение не поддерживает элементы управления вводом.</span><span class="sxs-lookup"><span data-stu-id="36f5e-112">Therefore, the word balloon does not support input controls.</span></span> <span data-ttu-id="36f5e-113">Однако можно легко предоставить ввод пользователя для символа, используя интерфейсы на языке программирования или другие входные службы, предоставляемые Microsoft Agent, такие как всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="36f5e-113">However, you can easily provide user input for a character, using interfaces from your programming language or the other input services provided by Microsoft Agent, such as the pop-up menu.</span></span>

<span data-ttu-id="36f5e-114">При определении символа можно указать, следует ли включать поддержку всплывающих окон в Word.</span><span class="sxs-lookup"><span data-stu-id="36f5e-114">When you define a character, you can specify whether to include word balloon support.</span></span> <span data-ttu-id="36f5e-115">Однако, если используется символ, включающий поддержку всплывающих подсказок Word, отключить поддержку невозможно.</span><span class="sxs-lookup"><span data-stu-id="36f5e-115">However, if you use a character that includes word balloon support, you cannot disable the support.</span></span>

 

 




