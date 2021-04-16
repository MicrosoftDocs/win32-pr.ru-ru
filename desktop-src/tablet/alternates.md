---
description: Альтернативой является возможное совпадение слов для сегмента распознавания. Распознаватель создает альтернативы и порождает их на допустимые совпадения рукописного ввода или звука с словарем или фактоид.
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: Варианты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350c9ac97f0af1451a0ded6445cf658dad4ee4c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662107"
---
# <a name="alternates"></a><span data-ttu-id="da196-104">Варианты</span><span class="sxs-lookup"><span data-stu-id="da196-104">Alternates</span></span>

<span data-ttu-id="da196-105">Альтернативой является возможное совпадение слов для сегмента распознавания.</span><span class="sxs-lookup"><span data-stu-id="da196-105">An alternate is a potential word match for a recognition segment.</span></span> <span data-ttu-id="da196-106">Распознаватель создает альтернативы и порождает их на допустимые совпадения рукописного ввода или звука с словарем или фактоид.</span><span class="sxs-lookup"><span data-stu-id="da196-106">A recognizer generates alternates and bases them on acceptable matches of the ink or audio input against a dictionary or factoid.</span></span>

> [!Note]  
> <span data-ttu-id="da196-107">Оценка достоверности в настоящее время доступна только для распознавателей Microsoft English (США) и жестов.</span><span class="sxs-lookup"><span data-stu-id="da196-107">Confidence evaluation is currently available only for the Microsoft English (United States) and gesture recognizers.</span></span>

 

<span data-ttu-id="da196-108">Иногда рукописные данные могут иметь неоднозначные различия между сегментами.</span><span class="sxs-lookup"><span data-stu-id="da196-108">Sometimes the ink may have ambiguous distinctions between segments.</span></span> <span data-ttu-id="da196-109">Распознаватель сравнивает эти сегменты с словарем распознавателя, чтобы определить возможные совпадения.</span><span class="sxs-lookup"><span data-stu-id="da196-109">The recognizer compares these segments to a recognizer dictionary to determine possible matches.</span></span> <span data-ttu-id="da196-110">Когда распознаватель сравнивает сегменты, он сохраняет список возможных альтернативных совпадений и назначает уровень достоверности каждому из них, выбрав верхний вариант.</span><span class="sxs-lookup"><span data-stu-id="da196-110">When the recognizer compares the segments, it maintains a list of possible alternate matches and assigns a confidence level to each one, picking a top choice.</span></span>

> [!Note]  
> <span data-ttu-id="da196-111">Распознаватель не может предоставить варианты для фрагмента рукописного ввода, который меньше, чем сегмент распознавания.</span><span class="sxs-lookup"><span data-stu-id="da196-111">The recognizer cannot provide alternates for a portion of ink that is smaller than a recognition segment.</span></span>

 

 

 



