---
description: В этом разделе описываются типы форматов для строк, используемых для формирования рисунка формата для строки времени. Каждое изображение формата состоит из комбинации одной строки каждого типа формата.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Изображения часов, минут и секунд формата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589c04fea0d6ce2f522436c30c39c873e3a7165e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081616"
---
# <a name="hour-minute-and-second-format-pictures"></a><span data-ttu-id="56f8b-104">Изображения часов, минут и секунд формата</span><span class="sxs-lookup"><span data-stu-id="56f8b-104">Hour, Minute, and Second Format Pictures</span></span>

<span data-ttu-id="56f8b-105">В этом разделе описываются типы форматов для строк, используемых для формирования рисунка формата для строки времени.</span><span class="sxs-lookup"><span data-stu-id="56f8b-105">This topic describes the format types for strings used to compose the format picture for a time string.</span></span> <span data-ttu-id="56f8b-106">Каждое изображение формата состоит из комбинации одной строки каждого типа формата.</span><span class="sxs-lookup"><span data-stu-id="56f8b-106">Each format picture consists of a combination of one string of each of the format types.</span></span>

> [!Note]  
> <span data-ttu-id="56f8b-107">В типах форматов буквы "m", "s" и "t" должны быть строчными, а буква "h" должна быть строчной для обозначения 12-часового времени или прописной буквы ("H") для обозначения 24-часового времени.</span><span class="sxs-lookup"><span data-stu-id="56f8b-107">In the format types, the letters "m", "s", and "t" must be lowercase, and the letter "h" must be lowercase to denote the 12-hour clock or uppercase ("H") to denote the 24-hour clock.</span></span>

<span data-ttu-id="56f8b-108">Одинарные кавычки можно использовать для пометки символов, которые должны отображаться в точности так, как указано.</span><span class="sxs-lookup"><span data-stu-id="56f8b-108">Single quotation marks can be used to mark characters that should be displayed exactly as specified.</span></span> <span data-ttu-id="56f8b-109">Если приложение должно отображать одинарные кавычки, оно должно содержать две одинарные кавычки в строке.</span><span class="sxs-lookup"><span data-stu-id="56f8b-109">If the application must display a single quotation mark, it should place two single quotation marks in a row.</span></span> <span data-ttu-id="56f8b-110">Например, "ABC" "Bar" отображается как "абк'бар".</span><span class="sxs-lookup"><span data-stu-id="56f8b-110">For example, 'abc''bar', is displayed as "abc'bar".</span></span>

<span data-ttu-id="56f8b-111">В следующей таблице определены типы форматов, используемые для представления часов.</span><span class="sxs-lookup"><span data-stu-id="56f8b-111">The following table defines the format types used to represent hours.</span></span>

| <span data-ttu-id="56f8b-112">Строка</span><span class="sxs-lookup"><span data-stu-id="56f8b-112">String</span></span> | <span data-ttu-id="56f8b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="56f8b-113">Meaning</span></span>                                                             |
|--------|---------------------------------------------------------------------|
| <span data-ttu-id="56f8b-114">h</span><span class="sxs-lookup"><span data-stu-id="56f8b-114">h</span></span>      | <span data-ttu-id="56f8b-115">Часы без начальных нулей для часов с одной цифрой (12-часовой формат).</span><span class="sxs-lookup"><span data-stu-id="56f8b-115">Hours without leading zeros for single-digit hours (12-hour clock).</span></span> |
| <span data-ttu-id="56f8b-116">hh</span><span class="sxs-lookup"><span data-stu-id="56f8b-116">hh</span></span>     | <span data-ttu-id="56f8b-117">Часы с начальными нулями для часов в одной цифре (12-часовой формат).</span><span class="sxs-lookup"><span data-stu-id="56f8b-117">Hours with leading zeros for single-digit hours (12-hour clock).</span></span>    |
| <span data-ttu-id="56f8b-118">H</span><span class="sxs-lookup"><span data-stu-id="56f8b-118">H</span></span>      | <span data-ttu-id="56f8b-119">Часы без начальных нулей для часов с одной цифрой (24-часовой формат).</span><span class="sxs-lookup"><span data-stu-id="56f8b-119">Hours without leading zeros for single-digit hours (24-hour clock).</span></span> |
| <span data-ttu-id="56f8b-120">HH</span><span class="sxs-lookup"><span data-stu-id="56f8b-120">HH</span></span>     | <span data-ttu-id="56f8b-121">Часы с начальными нулями для часов в одной цифре (24-часовой формат).</span><span class="sxs-lookup"><span data-stu-id="56f8b-121">Hours with leading zeros for single-digit hours (24-hour clock).</span></span>    |

<span data-ttu-id="56f8b-122">В следующей таблице определены типы форматов, используемые для представления минут.</span><span class="sxs-lookup"><span data-stu-id="56f8b-122">The following table defines the format types used to represent minutes.</span></span>

| <span data-ttu-id="56f8b-123">Строка</span><span class="sxs-lookup"><span data-stu-id="56f8b-123">String</span></span> | <span data-ttu-id="56f8b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="56f8b-124">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="56f8b-125">m</span><span class="sxs-lookup"><span data-stu-id="56f8b-125">m</span></span>      | <span data-ttu-id="56f8b-126">Минуты без начальных нулей для однозначных минут.</span><span class="sxs-lookup"><span data-stu-id="56f8b-126">Minutes without leading zeros for single-digit minutes.</span></span> |
| <span data-ttu-id="56f8b-127">ММ</span><span class="sxs-lookup"><span data-stu-id="56f8b-127">mm</span></span>     | <span data-ttu-id="56f8b-128">Минуты с начальными нулями для минут, состоящих из одной цифры.</span><span class="sxs-lookup"><span data-stu-id="56f8b-128">Minutes with leading zeros for single-digit minutes.</span></span>    |

<span data-ttu-id="56f8b-129">В следующей таблице определены типы форматов, используемые для представления секунд.</span><span class="sxs-lookup"><span data-stu-id="56f8b-129">The following table defines the format types used to represent seconds.</span></span>

| <span data-ttu-id="56f8b-130">Строка</span><span class="sxs-lookup"><span data-stu-id="56f8b-130">String</span></span> | <span data-ttu-id="56f8b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="56f8b-131">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="56f8b-132">s</span><span class="sxs-lookup"><span data-stu-id="56f8b-132">s</span></span>      | <span data-ttu-id="56f8b-133">Секунды без начальных нулей для однозначных секунд.</span><span class="sxs-lookup"><span data-stu-id="56f8b-133">Seconds without leading zeros for single-digit seconds.</span></span> |
| <span data-ttu-id="56f8b-134">сс</span><span class="sxs-lookup"><span data-stu-id="56f8b-134">ss</span></span>     | <span data-ttu-id="56f8b-135">Секунды с начальными нулями для однозначных секунд.</span><span class="sxs-lookup"><span data-stu-id="56f8b-135">Seconds with leading zeros for single-digit seconds.</span></span>    |

<span data-ttu-id="56f8b-136">В следующей таблице определяются типы форматов, используемые для представления маркера времени.</span><span class="sxs-lookup"><span data-stu-id="56f8b-136">The following table defines the format types used to represent a time marker.</span></span>

| <span data-ttu-id="56f8b-137">Строка</span><span class="sxs-lookup"><span data-stu-id="56f8b-137">String</span></span> | <span data-ttu-id="56f8b-138">Значение</span><span class="sxs-lookup"><span data-stu-id="56f8b-138">Meaning</span></span>|
| ---    | ---    |
| <span data-ttu-id="56f8b-139">t</span><span class="sxs-lookup"><span data-stu-id="56f8b-139">t</span></span>      | <span data-ttu-id="56f8b-140">Строка маркера времени из одного символа.</span><span class="sxs-lookup"><span data-stu-id="56f8b-140">One-character time marker string.</span></span><br /><span data-ttu-id="56f8b-141">**Примечание.** Этот формат не рекомендуется использовать с определенными языками, например японскими (Япония).</span><span class="sxs-lookup"><span data-stu-id="56f8b-141">**Note:** This format is not recommended for use with certain languages, such as Japanese (Japan).</span></span> <span data-ttu-id="56f8b-142">В этом формате приложение всегда принимает первый символ из строки маркера времени, определенного [LOCALE_S1159](locale-s1159.md) (AM) и [LOCALE_S2359](locale-s2359.md) (PM).</span><span class="sxs-lookup"><span data-stu-id="56f8b-142">With this format, an application always takes the first character from the time marker string, defined by [LOCALE_S1159](locale-s1159.md) (AM) and [LOCALE_S2359](locale-s2359.md) (PM).</span></span> <span data-ttu-id="56f8b-143">По этой причине приложение может создать неверное форматирование с той же строкой, что и для AM и PM.</span><span class="sxs-lookup"><span data-stu-id="56f8b-143">Because of this, the application can create incorrect formatting with the same string used for both AM and PM.</span></span>|
| <span data-ttu-id="56f8b-144">tt</span><span class="sxs-lookup"><span data-stu-id="56f8b-144">tt</span></span>     | <span data-ttu-id="56f8b-145">Строка многосимвольного маркера времени.</span><span class="sxs-lookup"><span data-stu-id="56f8b-145">Multi-character time marker string.</span></span> |
