---
description: Проверьте список значений режима преобразования редактора методов ввода (IME). Эти значения используются с функциями Иммжетконверсионстатус и Иммсетконверсионстатус.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Значения режима преобразования IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c52bc2f8f6f9fc87df48a15c66ce24b33e51742
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406757"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="d1624-104">Значения режима преобразования IME</span><span class="sxs-lookup"><span data-stu-id="d1624-104">IME Conversion Mode Values</span></span>

<span data-ttu-id="d1624-105">Эти значения используются с функциями [**иммжетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) и [**иммсетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="d1624-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="d1624-106">bit</span><span class="sxs-lookup"><span data-stu-id="d1624-106">Bit</span></span>                      | <span data-ttu-id="d1624-107">Значение</span><span class="sxs-lookup"><span data-stu-id="d1624-107">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1624-108">IME, \_ кмоде \_ буквенно-цифровой</span><span class="sxs-lookup"><span data-stu-id="d1624-108">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="d1624-109">Буквенно-цифровой режим ввода.</span><span class="sxs-lookup"><span data-stu-id="d1624-109">Alphanumeric input mode.</span></span> <span data-ttu-id="d1624-110">Это значение по умолчанию, определенное как символ 0x0000.</span><span class="sxs-lookup"><span data-stu-id="d1624-110">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="d1624-111">IME \_ кмоде \_ CHARCODE</span><span class="sxs-lookup"><span data-stu-id="d1624-111">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="d1624-112">Значение 1, если режим ввода кода символа; 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="d1624-112">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="d1624-113">IME \_ кмоде \_ EUDC</span><span class="sxs-lookup"><span data-stu-id="d1624-113">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="d1624-114">Задайте значение 1, если режим преобразования EUDC. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="d1624-114">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="d1624-115">\_КМОДЕ IME \_ fixed</span><span class="sxs-lookup"><span data-stu-id="d1624-115">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="d1624-116">Windows **Me/98, windows 2000, Windows XP:** При фиксированном режиме преобразования задайте значение 1. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="d1624-116">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="d1624-117">редактор IME \_ кмоде \_ фуллшапе</span><span class="sxs-lookup"><span data-stu-id="d1624-117">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="d1624-118">Задайте значение 1, если режим полной формы; 0, если режим половинной фигуры.</span><span class="sxs-lookup"><span data-stu-id="d1624-118">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="d1624-119">редактор IME \_ кмоде \_ ханжаконверт</span><span class="sxs-lookup"><span data-stu-id="d1624-119">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="d1624-120">Задайте значение 1 в режиме преобразования ХАНДЖА. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="d1624-120">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="d1624-121">IME \_ кмоде \_ катакана</span><span class="sxs-lookup"><span data-stu-id="d1624-121">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="d1624-122">Задайте значение 1 в режиме катакана. 0, если режим хирагана.</span><span class="sxs-lookup"><span data-stu-id="d1624-122">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="d1624-123">\_КМОДЕ IME \_ native</span><span class="sxs-lookup"><span data-stu-id="d1624-123">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="d1624-124">Задайте значение 1, если собственный режим —. 0, если БУКВЕНно-цифровой режим.</span><span class="sxs-lookup"><span data-stu-id="d1624-124">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="d1624-125">\_КМОДЕ IME \_</span><span class="sxs-lookup"><span data-stu-id="d1624-125">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="d1624-126">Задайте значение 1, чтобы предотвратить обработку преобразований IME. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="d1624-126">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="d1624-127">IME \_ кмоде \_ Roman</span><span class="sxs-lookup"><span data-stu-id="d1624-127">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="d1624-128">Задайте значение 1 в режиме ввода ЛАТИНИЦЫ. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="d1624-128">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="d1624-129">редактор IME \_ кмоде \_ софткбд</span><span class="sxs-lookup"><span data-stu-id="d1624-129">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="d1624-130">Задайте значение 1 в режиме экранной клавиатуры. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="d1624-130">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="d1624-131">\_символ КМОДЕ \_ IME</span><span class="sxs-lookup"><span data-stu-id="d1624-131">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="d1624-132">В режиме преобразования символов задайте значение 1. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="d1624-132">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="d1624-133">Все остальные биты зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="d1624-133">All other bits are reserved.</span></span>

 

 



