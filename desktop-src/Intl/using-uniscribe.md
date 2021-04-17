---
description: Uniscribe предоставляет API-интерфейсы для поддержки оформления, а также для поддержки просмотра и редактирования международного текста, включая сложные правила средних и восточно-азиатских символов.
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: Использование Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dcfcd602940c04aa8615d141dd9a83db1fa2e55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674439"
---
# <a name="using-uniscribe"></a><span data-ttu-id="ba099-103">Использование Uniscribe</span><span class="sxs-lookup"><span data-stu-id="ba099-103">Using Uniscribe</span></span>

<span data-ttu-id="ba099-104">Uniscribe предоставляет API-интерфейсы для поддержки оформления, а также для поддержки просмотра и редактирования международного текста, включая сложные правила средних и восточно-азиатских символов.</span><span class="sxs-lookup"><span data-stu-id="ba099-104">Uniscribe provides APIs to support typography and to support the display and editing of international text, including the complex rules of Middle Eastern and Asian scripts.</span></span> <span data-ttu-id="ba099-105">Uniscribe предоставляет низкоуровневые подпрограммы для обработки полностью отформатированного текста и простой Скриптстринг API для неформатированного текста.</span><span class="sxs-lookup"><span data-stu-id="ba099-105">Uniscribe provides low-level routines for handling fully formatted text, and a simple ScriptString API set for unformatted text.</span></span>

<span data-ttu-id="ba099-106">С помощью Uniscribe приложения должны управлять резервным хранилищем кодов символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="ba099-106">Using Uniscribe, applications only have to manage a backing store of Unicode character codes.</span></span> <span data-ttu-id="ba099-107">Приложениям макета текста не требуется сохранять другие буферы или таблицы сопоставлений для отслеживания порядка символов.</span><span class="sxs-lookup"><span data-stu-id="ba099-107">Text layout applications do not have to maintain any other buffer or mapping table to track character order.</span></span> <span data-ttu-id="ba099-108">Каждое приложение должно хранить и управлять порядком, в котором символы записываются пользователем. это тот же логический порядок, который определен в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="ba099-108">Each application only has to store and manage the order in which the characters are entered by the user, which is the same logical order as defined by Unicode.</span></span> <span data-ttu-id="ba099-109">Резервное хранилище никогда не изменяется в результате операций макета.</span><span class="sxs-lookup"><span data-stu-id="ba099-109">The backing store never changes as a result of layout operations.</span></span> <span data-ttu-id="ba099-110">Uniscribe сохраняет индекс из переупорядоченных кластеров до исходных границ символов, переданных приложением.</span><span class="sxs-lookup"><span data-stu-id="ba099-110">Uniscribe maintains an index from the reordered clusters to the original character boundaries passed by the application.</span></span>

<span data-ttu-id="ba099-111">В этом разделе рассматриваются следующие темы.</span><span class="sxs-lookup"><span data-stu-id="ba099-111">The following topics are covered in this section.</span></span>

<span data-ttu-id="ba099-112">**Формирование**</span><span class="sxs-lookup"><span data-stu-id="ba099-112">**Shaping**</span></span>

-   [<span data-ttu-id="ba099-113">Определение, требует ли сценарий формирования глифов</span><span class="sxs-lookup"><span data-stu-id="ba099-113">Determining If a Script Requires Glyph Shaping</span></span>](determining-if-a-script-requires-glyph-shaping.md)
-   [<span data-ttu-id="ba099-114">Использование механизмов формирования</span><span class="sxs-lookup"><span data-stu-id="ba099-114">Using Shaping Engines</span></span>](using-shaping-engines.md)

<span data-ttu-id="ba099-115">**Другая обработка**</span><span class="sxs-lookup"><span data-stu-id="ba099-115">**Other Processing**</span></span>

-   [<span data-ttu-id="ba099-116">Кэширование</span><span class="sxs-lookup"><span data-stu-id="ba099-116">Caching</span></span>](caching.md)
-   [<span data-ttu-id="ba099-117">Отображение текста с помощью Uniscribe</span><span class="sxs-lookup"><span data-stu-id="ba099-117">Displaying Text with Uniscribe</span></span>](displaying-text-with-uniscribe.md)
-   [<span data-ttu-id="ba099-118">Обработка сложных наборов символов</span><span class="sxs-lookup"><span data-stu-id="ba099-118">Processing Complex Scripts</span></span>](processing-complex-scripts.md)
-   [<span data-ttu-id="ba099-119">Использование отката шрифта</span><span class="sxs-lookup"><span data-stu-id="ba099-119">Using Font Fallback</span></span>](using-font-fallback.md)
-   [<span data-ttu-id="ba099-120">Использование функций Скриптстринг</span><span class="sxs-lookup"><span data-stu-id="ba099-120">Using the ScriptString Functions</span></span>](using-the-scriptstring-functions.md)

<span data-ttu-id="ba099-121">**Курсор**</span><span class="sxs-lookup"><span data-stu-id="ba099-121">**Caret**</span></span>

-   [<span data-ttu-id="ba099-122">Отображение курсора в двунаправленных строках</span><span class="sxs-lookup"><span data-stu-id="ba099-122">Displaying the Caret in Bidirectional Strings</span></span>](displaying-the-caret-in-bidirectional-strings.md)
-   [<span data-ttu-id="ba099-123">Управление размещением курсора и проверкой попадания</span><span class="sxs-lookup"><span data-stu-id="ba099-123">Managing Caret Placement and Hit Testing</span></span>](managing-caret-placement-and-hit-testing.md)
-   [<span data-ttu-id="ba099-124">Смещение нажатия кнопки мыши X в позиции курсора</span><span class="sxs-lookup"><span data-stu-id="ba099-124">Translating Mouse Hit X Offset to Caret Position</span></span>](translating-mouse-hit-x-offset-to-caret-position.md)

<span data-ttu-id="ba099-125">**Слова и кластеры символов**</span><span class="sxs-lookup"><span data-stu-id="ba099-125">**Words and Character Clusters**</span></span>

-   [<span data-ttu-id="ba099-126">Использование кластеров символов</span><span class="sxs-lookup"><span data-stu-id="ba099-126">Using Character Clusters</span></span>](using-character-clusters.md)
-   [<span data-ttu-id="ba099-127">Использование точек останова Word</span><span class="sxs-lookup"><span data-stu-id="ba099-127">Using Word Break Points</span></span>](using-word-break-points.md)
-   [<span data-ttu-id="ba099-128">Работа со связями между позициями курсора, точками обоснования и кластерами</span><span class="sxs-lookup"><span data-stu-id="ba099-128">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



