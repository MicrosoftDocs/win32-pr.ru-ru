---
description: инегативеперцент ЛОКАЛи \_
ms.assetid: 3518bd71-631d-48f2-b17f-b2ed41d44484
title: LOCALE_INEGATIVEPERCENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b98ee0229dfbbd392fbc03d2a7b5e4b413b3fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991585"
---
# <a name="locale_inegativepercent"></a><span data-ttu-id="e24fc-103">инегативеперцент ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="e24fc-103">LOCALE\_INEGATIVEPERCENT</span></span>

<span data-ttu-id="e24fc-104">**Windows 7 и более поздние версии:** Шаблон форматирования отрицательного процента для языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="e24fc-104">**Windows 7 and later:** Negative percentage formatting pattern for the locale.</span></span> <span data-ttu-id="e24fc-105">Может быть указан только один шаблон.</span><span class="sxs-lookup"><span data-stu-id="e24fc-105">Only one pattern can be indicated.</span></span> <span data-ttu-id="e24fc-106">Если для языкового стандарта используется более одного формата, выберите вариант предпочтительно.</span><span class="sxs-lookup"><span data-stu-id="e24fc-106">If more than one format is used for the locale, choose the preferred option.</span></span> <span data-ttu-id="e24fc-107">Например, если в качестве отрицательного процентного значения отображается «-9%» для «отрицательных девяти процентов», то для этой константы нужно выбрать значение 0.</span><span class="sxs-lookup"><span data-stu-id="e24fc-107">For example, if a negative percentage is displayed "-9 %" for "negative nine percent", the appropriate choice for this constant is 0.</span></span>



| <span data-ttu-id="e24fc-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e24fc-108">Value</span></span> | <span data-ttu-id="e24fc-109">Формат</span><span class="sxs-lookup"><span data-stu-id="e24fc-109">Format</span></span>                                                    |
|-------|-----------------------------------------------------------|
| <span data-ttu-id="e24fc-110">0</span><span class="sxs-lookup"><span data-stu-id="e24fc-110">0</span></span>     | <span data-ttu-id="e24fc-111">Отрицательный знак, число, пробел, процент; Например,-\# %</span><span class="sxs-lookup"><span data-stu-id="e24fc-111">Negative sign, number, space, percent; for example, -\# %</span></span> |
| <span data-ttu-id="e24fc-112">1</span><span class="sxs-lookup"><span data-stu-id="e24fc-112">1</span></span>     | <span data-ttu-id="e24fc-113">Отрицательный знак, число, процент; Например,-\#%</span><span class="sxs-lookup"><span data-stu-id="e24fc-113">Negative sign, number, percent; for example, -\#%</span></span>         |
| <span data-ttu-id="e24fc-114">2</span><span class="sxs-lookup"><span data-stu-id="e24fc-114">2</span></span>     | <span data-ttu-id="e24fc-115">Отрицательный знак, процент, число; Например,-%\#</span><span class="sxs-lookup"><span data-stu-id="e24fc-115">Negative sign, percent, number; for example, -%\#</span></span>         |
| <span data-ttu-id="e24fc-116">3</span><span class="sxs-lookup"><span data-stu-id="e24fc-116">3</span></span>     | <span data-ttu-id="e24fc-117">Процент, знак минус, число; Например,%-\#</span><span class="sxs-lookup"><span data-stu-id="e24fc-117">Percent, negative sign, number; for example, %-\#</span></span>         |
| <span data-ttu-id="e24fc-118">4</span><span class="sxs-lookup"><span data-stu-id="e24fc-118">4</span></span>     | <span data-ttu-id="e24fc-119">Процент, число, отрицательный знак; Например,%\#-</span><span class="sxs-lookup"><span data-stu-id="e24fc-119">Percent, number, negative sign; for example, %\#-</span></span>         |
| <span data-ttu-id="e24fc-120">5</span><span class="sxs-lookup"><span data-stu-id="e24fc-120">5</span></span>     | <span data-ttu-id="e24fc-121">Число, знак минус, процент; Например \#-%</span><span class="sxs-lookup"><span data-stu-id="e24fc-121">Number, negative sign, percent; for example, \#-%</span></span>         |
| <span data-ttu-id="e24fc-122">6</span><span class="sxs-lookup"><span data-stu-id="e24fc-122">6</span></span>     | <span data-ttu-id="e24fc-123">Число, процент, знак минус; Например \#%-</span><span class="sxs-lookup"><span data-stu-id="e24fc-123">Number, percent, negative sign; for example, \#%-</span></span>         |
| <span data-ttu-id="e24fc-124">7</span><span class="sxs-lookup"><span data-stu-id="e24fc-124">7</span></span>     | <span data-ttu-id="e24fc-125">Отрицательный знак, процент, пробел, число; Например,-% \#</span><span class="sxs-lookup"><span data-stu-id="e24fc-125">Negative sign, percent, space, number; for example, -% \#</span></span> |
| <span data-ttu-id="e24fc-126">8</span><span class="sxs-lookup"><span data-stu-id="e24fc-126">8</span></span>     | <span data-ttu-id="e24fc-127">Число, пробел, процент, знак минус; Например \# %-</span><span class="sxs-lookup"><span data-stu-id="e24fc-127">Number, space, percent, negative sign; for example, \# %-</span></span> |
| <span data-ttu-id="e24fc-128">9</span><span class="sxs-lookup"><span data-stu-id="e24fc-128">9</span></span>     | <span data-ttu-id="e24fc-129">Процент, пробел, число, знак минус; Например,% \#-</span><span class="sxs-lookup"><span data-stu-id="e24fc-129">Percent, space, number, negative sign; for example, % \#-</span></span> |
| <span data-ttu-id="e24fc-130">10</span><span class="sxs-lookup"><span data-stu-id="e24fc-130">10</span></span>    | <span data-ttu-id="e24fc-131">Процент, пробел, знак минус, число; Например,%-\#</span><span class="sxs-lookup"><span data-stu-id="e24fc-131">Percent, space, negative sign, number; for example, % -\#</span></span> |
| <span data-ttu-id="e24fc-132">11</span><span class="sxs-lookup"><span data-stu-id="e24fc-132">11</span></span>    | <span data-ttu-id="e24fc-133">Число, отрицательный знак, пробел, процент; Например, \# -%</span><span class="sxs-lookup"><span data-stu-id="e24fc-133">Number, negative sign, space, percent; for example, \#- %</span></span> |



 

 

 



