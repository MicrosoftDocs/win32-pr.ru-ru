---
description: Сегмент распознавания — это базовая единица рукописного ввода, которую распознаватель использует для получения результатов распознавания определенного объекта рукописного ввода.
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: Сегменты распознавания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703046"
---
# <a name="recognition-segments"></a><span data-ttu-id="af97d-103">Сегменты распознавания</span><span class="sxs-lookup"><span data-stu-id="af97d-103">Recognition Segments</span></span>

<span data-ttu-id="af97d-104">Сегмент распознавания — это базовая единица рукописного ввода, которую распознаватель использует для получения результатов распознавания определенного объекта рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="af97d-104">A recognition segment is the basic ink unit that a recognizer uses internally to produce a recognition result for a particular Ink object.</span></span> <span data-ttu-id="af97d-105">Сегмент распознавания — это коллекция рукописных штрихов.</span><span class="sxs-lookup"><span data-stu-id="af97d-105">A recognition segment is a collection of ink strokes.</span></span> <span data-ttu-id="af97d-106">Например, распознаватель, способный распознать письменное письмо на английском языке, может использовать слово в качестве основного сегмента распознавания.</span><span class="sxs-lookup"><span data-stu-id="af97d-106">For example, a recognizer that is capable of recognizing English cursive handwriting might use a word as the basic recognition segment.</span></span>

<span data-ttu-id="af97d-107">Другие распознаватели могут использовать части составных слов в качестве основных сегментов.</span><span class="sxs-lookup"><span data-stu-id="af97d-107">Other recognizers may use parts of composite words as basic segments.</span></span> <span data-ttu-id="af97d-108">Например, в испанском языке короткие слова обычно объединяются для предоставления более длинных составных слов.</span><span class="sxs-lookup"><span data-stu-id="af97d-108">For example, in Spanish, short words are commonly combined to provide longer composite words.</span></span> <span data-ttu-id="af97d-109">"Дамело" — это испанское слово, состоящее из трех слов "Da Me" (дайте мне это), но написано как одно слово.</span><span class="sxs-lookup"><span data-stu-id="af97d-109">"Damelo" is a Spanish word that is composed of three words "da me lo" (give me that), but it is written as a single word.</span></span> <span data-ttu-id="af97d-110">Распознаватель на испанском языке может распознать каждое подслово как сегмент.</span><span class="sxs-lookup"><span data-stu-id="af97d-110">A Spanish recognizer could recognize each subword as a segment.</span></span>

<span data-ttu-id="af97d-111">Распознаватель может найти несколько способов разбить образец рукописного ввода на сегменты распознавания.</span><span class="sxs-lookup"><span data-stu-id="af97d-111">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="af97d-112">Так как неоднозначность вовлечена в распознавание предполагаемых входных данных пользователя, распознаватель может возвращать множество альтернативных совпадений.</span><span class="sxs-lookup"><span data-stu-id="af97d-112">Because ambiguity is involved in recognizing the user's intended input, the recognizer can return many alternate matches.</span></span>

<span data-ttu-id="af97d-113">Дополнительные сведения об альтернативных вариантах см. в разделе [варианты](alternates.md).</span><span class="sxs-lookup"><span data-stu-id="af97d-113">For more information about alternates, see [Alternates](alternates.md).</span></span>

 

 



