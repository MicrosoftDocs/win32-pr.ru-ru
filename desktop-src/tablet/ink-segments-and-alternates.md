---
description: Распознаватель может найти несколько способов разбить образец рукописного ввода на сегменты распознавания. По этой причине количество вариантов распознавания может располагаться в шахматном порядке, даже для небольшого примера рукописного ввода.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Сегменты и варианты рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91183f6c9628ea798b66d703a59e44b26049e692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072721"
---
# <a name="ink-segments-and-alternates"></a><span data-ttu-id="7a824-104">Сегменты и варианты рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="7a824-104">Ink Segments and Alternates</span></span>

<span data-ttu-id="7a824-105">Распознаватель может найти несколько способов разбить образец рукописного ввода на сегменты распознавания.</span><span class="sxs-lookup"><span data-stu-id="7a824-105">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="7a824-106">По этой причине количество вариантов распознавания может располагаться в шахматном порядке, даже для небольшого примера рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="7a824-106">Because of this, the number of recognition alternates may be staggering, even for a small ink sample.</span></span>

<span data-ttu-id="7a824-107">Например, «t o g e t h e r» может привести к следующим результатам:</span><span class="sxs-lookup"><span data-stu-id="7a824-107">For example, "t o g e t h e r" can yield the following results:</span></span>

-   <span data-ttu-id="7a824-108">"чтобы получить его" (плюс альтернативные варианты для каждого слова)</span><span class="sxs-lookup"><span data-stu-id="7a824-108">"to get her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="7a824-109">"для сбора" (плюс альтернативные варианты для каждого слова)</span><span class="sxs-lookup"><span data-stu-id="7a824-109">"to gather" (plus alternates for each word)</span></span>
-   <span data-ttu-id="7a824-110">"тог Ether" (плюс альтернативные варианты для каждого слова)</span><span class="sxs-lookup"><span data-stu-id="7a824-110">"tog ether" (plus alternates for each word)</span></span>
-   <span data-ttu-id="7a824-111">«Тог» (плюс альтернативные варианты для каждого слова)</span><span class="sxs-lookup"><span data-stu-id="7a824-111">"tog at her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="7a824-112">"вместе" (плюс альтернативы для слова)</span><span class="sxs-lookup"><span data-stu-id="7a824-112">"together" (plus alternates for the word)</span></span>

<span data-ttu-id="7a824-113">Объект [**рекогнитионресулт**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) поддерживает эффективное хранение полных результатов распознавания в объекте [**рукописного ввода**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="7a824-113">The [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object supports efficient storage of full recognition results within the [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="7a824-114">Объект **рукописного ввода** сопоставляет варианты распознавания с штрихами в объекте **рукописного ввода** и может также содержать другие сведения, такие как базовая линия, индексы строк и диапазоны языков.</span><span class="sxs-lookup"><span data-stu-id="7a824-114">The **Ink** object maps the recognition alternates to the strokes in the **Ink** object and may also contain other information such as baseline position, line indices, and language ranges.</span></span>

 

 



