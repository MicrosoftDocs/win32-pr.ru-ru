---
description: Файлы шрифтов TrueType содержат номера PANOSE, которые могут использоваться приложениями для выбора шрифта, близко соответствующего его спецификациям.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Использование номеров PANOSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfa6a185e2afb05aec5fdf0e200300c7cf686a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266187"
---
# <a name="using-panose-numbers"></a><span data-ttu-id="31b66-103">Использование номеров PANOSE</span><span class="sxs-lookup"><span data-stu-id="31b66-103">Using PANOSE Numbers</span></span>

<span data-ttu-id="31b66-104">Файлы шрифтов TrueType содержат номера PANOSE, которые могут использоваться приложениями для выбора шрифта, близко соответствующего его спецификациям.</span><span class="sxs-lookup"><span data-stu-id="31b66-104">TrueType font files include PANOSE numbers, which applications can use to choose a font that closely matches their specifications.</span></span> <span data-ttu-id="31b66-105">Система PANOSE классифицирует лиц на 10 различных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="31b66-105">The PANOSE system classifies faces by 10 different attributes.</span></span> <span data-ttu-id="31b66-106">Дополнительные сведения об этих атрибутах см. в разделе [**Panose**](/windows/win32/api/wingdi/ns-wingdi-panose).</span><span class="sxs-lookup"><span data-stu-id="31b66-106">For more information about these attributes, see [**PANOSE**](/windows/win32/api/wingdi/ns-wingdi-panose).</span></span> <span data-ttu-id="31b66-107">Структура **Panose** является частью структуры [**аутлинетекстметрик**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (значения которой заполняются путем вызова функции [**жетаутлинетекстметрикс**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) ).</span><span class="sxs-lookup"><span data-stu-id="31b66-107">A **PANOSE** structure is part of the [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) structure (whose values are filled in by calling the [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) function).</span></span>

<span data-ttu-id="31b66-108">Атрибуты PANOSE оцениваются по отдельности на шкале.</span><span class="sxs-lookup"><span data-stu-id="31b66-108">The PANOSE attributes are rated individually on a scale.</span></span> <span data-ttu-id="31b66-109">Результирующие значения объединяются для получения числа.</span><span class="sxs-lookup"><span data-stu-id="31b66-109">The resulting values are concatenated to produce a number.</span></span> <span data-ttu-id="31b66-110">Учитывая это число для шрифта и математическую метрику для измерения расстояний в PANOSE пространстве, приложение может определить соседних соседей.</span><span class="sxs-lookup"><span data-stu-id="31b66-110">Given this number for a font and a mathematical metric to measure distances in the PANOSE space, an application can determine the nearest neighbors.</span></span>

 

 



