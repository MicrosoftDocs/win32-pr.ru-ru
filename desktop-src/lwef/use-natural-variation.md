---
title: Использовать естественный вариант
description: Использовать естественный вариант
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd2d35afeb168dc8839ba259f0079434b487c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132874"
---
# <a name="use-natural-variation"></a><span data-ttu-id="cfef5-103">Использовать естественный вариант</span><span class="sxs-lookup"><span data-stu-id="cfef5-103">Use Natural Variation</span></span>

<span data-ttu-id="cfef5-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cfef5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="cfef5-105">Согласованность представления в обычном интерфейсе приложения, например меню и диалоговых окнах, делает интерфейс более предсказуемым, изменяя анимацию и речевые выходные данные в интерфейсе символа.</span><span class="sxs-lookup"><span data-stu-id="cfef5-105">While consistency of presentation in your application's conventional interface, such as menus and dialog boxes, makes the interface more predictable, vary the animation and spoken output in the character's interface.</span></span> <span data-ttu-id="cfef5-106">Соответствующим образом менять ответы на символы предоставляют более естественный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="cfef5-106">Appropriately varying the character's responses provides a more natural interface.</span></span> <span data-ttu-id="cfef5-107">Если символ всегда обращается к пользователю точно таким же образом; Например, всегда говорят о одних и тех же словах, пользователь, скорее всего, будет считать символ скучным, дисинтерестед или даже грубым.</span><span class="sxs-lookup"><span data-stu-id="cfef5-107">If a character always addresses the user exactly the same way; for example, always saying the same words, the user is likely to consider the character boring, disinterested, or even rude.</span></span> <span data-ttu-id="cfef5-108">Взаимодействие с человеком редко подразумевает точное повторение.</span><span class="sxs-lookup"><span data-stu-id="cfef5-108">Human communication rarely involves precise repetition.</span></span> <span data-ttu-id="cfef5-109">Даже при повторении чего-то в подобной ситуации мы можем изменить слова, жесты или выражение лица.</span><span class="sxs-lookup"><span data-stu-id="cfef5-109">Even when repeating something in a similar situation, we may change wording, gestures, or facial expression.</span></span>

<span data-ttu-id="cfef5-110">Microsoft Agent позволяет создавать отдельные варианты для символа.</span><span class="sxs-lookup"><span data-stu-id="cfef5-110">Microsoft Agent enables you to build in some variation for a character.</span></span> <span data-ttu-id="cfef5-111">При определении анимации символа можно использовать вероятности ветвления в любом кадре анимации, чтобы изменить анимацию при ее воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="cfef5-111">When defining a character's animations, you can use branching probabilities on any animation frame to change an animation when it plays.</span></span> <span data-ttu-id="cfef5-112">Можно также назначить несколько анимаций для каждого состояния.</span><span class="sxs-lookup"><span data-stu-id="cfef5-112">You can also assign multiple animations to each state.</span></span> <span data-ttu-id="cfef5-113">Microsoft Agent случайным образом выбирает одну из назначенных анимаций при каждом запуске состояния.</span><span class="sxs-lookup"><span data-stu-id="cfef5-113">Microsoft Agent randomly chooses one of the assigned animations each time it initiates a state.</span></span> <span data-ttu-id="cfef5-114">Для речевого вывода можно также включить в выходной текст символы вертикальной черты, чтобы автоматически изменять текст.</span><span class="sxs-lookup"><span data-stu-id="cfef5-114">For speech output, you can also include vertical bar characters in your output text to automatically vary the text spoken.</span></span> <span data-ttu-id="cfef5-115">Например, Microsoft Agent случайным образом выберет одну из следующих инструкций при обработке этого текста как части метода [**говорите**](speak-method.md) :</span><span class="sxs-lookup"><span data-stu-id="cfef5-115">For example, Microsoft Agent will randomly select one of the following statements when processing this text as part of the [**Speak**](speak-method.md) method:</span></span>

<span data-ttu-id="cfef5-116">«Я могу сказать это. \| Я могу сказать, что. \| Я могу сказать что-то другое».</span><span class="sxs-lookup"><span data-stu-id="cfef5-116">"I can say this.\|I can say that.\|I can say something else."</span></span>

 

 




