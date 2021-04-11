---
description: идигитсубститутион ЛОКАЛи \_
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143453"
---
# <a name="locale_idigitsubstitution"></a><span data-ttu-id="f688d-103">идигитсубститутион ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="f688d-103">LOCALE\_IDIGITSUBSTITUTION</span></span>

<span data-ttu-id="f688d-104">**Windows 2000:** Форма цифр.</span><span class="sxs-lookup"><span data-stu-id="f688d-104">**Windows 2000:** The shape of digits.</span></span> <span data-ttu-id="f688d-105">Например, в арабском, тайском и индийских цифрах классические фигуры отличаются от европейских цифр.</span><span class="sxs-lookup"><span data-stu-id="f688d-105">For example, Arabic, Thai, and Indic digits have classical shapes different from European digits.</span></span> <span data-ttu-id="f688d-106">Для [языковых стандартов с \_ Снативедигитсом локали](locale-snative-constants.md) , заданными как значения, отличные от ASCII 0-9, это значение указывает, следует ли предоставлять предпочтение другим цифрам в целях показа.</span><span class="sxs-lookup"><span data-stu-id="f688d-106">For locales with [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) specified as values other than ASCII 0-9, this value specifies whether preference should be given to those other digits for display purposes.</span></span> <span data-ttu-id="f688d-107">Например, если выбрано значение 2, то всегда используются цифры, заданные параметром LOCALE \_ снативедигитс.</span><span class="sxs-lookup"><span data-stu-id="f688d-107">For example, if a value of 2 is chosen, the digits specified by LOCALE\_SNATIVEDIGITS are always used.</span></span> <span data-ttu-id="f688d-108">Если выбрано значение 1, то всегда используются цифры ASCII 0-9.</span><span class="sxs-lookup"><span data-stu-id="f688d-108">If a 1 is chosen, the ASCII 0-9 digits are always used.</span></span> <span data-ttu-id="f688d-109">Если выбрано значение 0, в некоторых обстоятельствах используется ASCII, а цифры, заданные параметром LOCALE \_ снативедигитс, используются в других, в зависимости от контекста.</span><span class="sxs-lookup"><span data-stu-id="f688d-109">If a 0 is chosen, ASCII is used in some circumstances and the digits specified by LOCALE\_SNATIVEDIGITS are used in others, depending on the context.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f688d-110">Значение</span><span class="sxs-lookup"><span data-stu-id="f688d-110">Value</span></span></th>
<th><span data-ttu-id="f688d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="f688d-111">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f688d-112">0</span><span class="sxs-lookup"><span data-stu-id="f688d-112">0</span></span></td>
<td><span data-ttu-id="f688d-113">Подстановка на основе контекста.</span><span class="sxs-lookup"><span data-stu-id="f688d-113">Context-based substitution.</span></span> <span data-ttu-id="f688d-114">Цифры отображаются на основе предыдущего текста в том же выводе.</span><span class="sxs-lookup"><span data-stu-id="f688d-114">Digits are displayed based on the previous text in the same output.</span></span> <span data-ttu-id="f688d-115">Европейские цифры следуют правилам латиницы, Arabic-Indic цифры следуют арабским текстам, а другие национальные цифры следуют тексту, написанному в различных сценариях.</span><span class="sxs-lookup"><span data-stu-id="f688d-115">European digits follow Latin scripts, Arabic-Indic digits follow Arabic text, and other national digits follow text written in various other scripts.</span></span> <span data-ttu-id="f688d-116">Если предшествующего текста нет, языковой стандарт и отображаемый порядок чтения определяют подстановку цифр, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f688d-116">When there is no preceding text, the locale and the displayed reading order determine digit substitution, as shown in the following table.</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f688d-117">Locale</span><span class="sxs-lookup"><span data-stu-id="f688d-117">Locale</span></span></th>
<th><span data-ttu-id="f688d-118">Порядок чтения</span><span class="sxs-lookup"><span data-stu-id="f688d-118">Reading order</span></span></th>
<th><span data-ttu-id="f688d-119">Используемые цифры</span><span class="sxs-lookup"><span data-stu-id="f688d-119">Digits used</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f688d-120">Арабский</span><span class="sxs-lookup"><span data-stu-id="f688d-120">Arabic</span></span></td>
<td><span data-ttu-id="f688d-121">Справа налево</span><span class="sxs-lookup"><span data-stu-id="f688d-121">Right-to-left</span></span></td>
<td><span data-ttu-id="f688d-122">Индо-арабская система счисления</span><span class="sxs-lookup"><span data-stu-id="f688d-122">Arabic-Indic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f688d-123">Тайский</span><span class="sxs-lookup"><span data-stu-id="f688d-123">Thai</span></span></td>
<td><span data-ttu-id="f688d-124">Слева направо</span><span class="sxs-lookup"><span data-stu-id="f688d-124">Left-to-right</span></span></td>
<td><span data-ttu-id="f688d-125">Тайские цифры</span><span class="sxs-lookup"><span data-stu-id="f688d-125">Thai digits</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f688d-126">Все остальные</span><span class="sxs-lookup"><span data-stu-id="f688d-126">All others</span></span></td>
<td><span data-ttu-id="f688d-127">Любой</span><span class="sxs-lookup"><span data-stu-id="f688d-127">Any</span></span></td>
<td><span data-ttu-id="f688d-128">Подстановка не используется</span><span class="sxs-lookup"><span data-stu-id="f688d-128">No substitution used</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f688d-129">1</span><span class="sxs-lookup"><span data-stu-id="f688d-129">1</span></span></td>
<td><span data-ttu-id="f688d-130">Подстановка не используется.</span><span class="sxs-lookup"><span data-stu-id="f688d-130">No substitution used.</span></span> <span data-ttu-id="f688d-131">Полная совместимость с Юникодом.</span><span class="sxs-lookup"><span data-stu-id="f688d-131">Full Unicode compatibility.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f688d-132">2</span><span class="sxs-lookup"><span data-stu-id="f688d-132">2</span></span></td>
<td><span data-ttu-id="f688d-133">Подстановка собственных цифр.</span><span class="sxs-lookup"><span data-stu-id="f688d-133">Native digit substitution.</span></span> <span data-ttu-id="f688d-134">Национальные фигуры отображаются в соответствии с LOCALE_SNATIVEDIGITS.</span><span class="sxs-lookup"><span data-stu-id="f688d-134">National shapes are displayed according to LOCALE_SNATIVEDIGITS.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



