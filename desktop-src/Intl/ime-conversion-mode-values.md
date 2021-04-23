---
description: Эти значения используются с функциями Иммжетконверсионстатус и Иммсетконверсионстатус.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Значения режима преобразования IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59b9f1a8d5015e78a5249d3499fc55e1a94d941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154586"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="81550-103">Значения режима преобразования IME</span><span class="sxs-lookup"><span data-stu-id="81550-103">IME Conversion Mode Values</span></span>

<span data-ttu-id="81550-104">Эти значения используются с функциями [**иммжетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) и [**иммсетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="81550-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="81550-105">bit</span><span class="sxs-lookup"><span data-stu-id="81550-105">Bit</span></span>                      | <span data-ttu-id="81550-106">Значение</span><span class="sxs-lookup"><span data-stu-id="81550-106">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="81550-107">IME, \_ кмоде \_ буквенно-цифровой</span><span class="sxs-lookup"><span data-stu-id="81550-107">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="81550-108">Буквенно-цифровой режим ввода.</span><span class="sxs-lookup"><span data-stu-id="81550-108">Alphanumeric input mode.</span></span> <span data-ttu-id="81550-109">Это значение по умолчанию, определенное как символ 0x0000.</span><span class="sxs-lookup"><span data-stu-id="81550-109">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="81550-110">IME \_ кмоде \_ CHARCODE</span><span class="sxs-lookup"><span data-stu-id="81550-110">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="81550-111">Значение 1, если режим ввода кода символа; 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="81550-111">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="81550-112">IME \_ кмоде \_ EUDC</span><span class="sxs-lookup"><span data-stu-id="81550-112">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="81550-113">Задайте значение 1, если режим преобразования EUDC. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="81550-113">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="81550-114">\_КМОДЕ IME \_ fixed</span><span class="sxs-lookup"><span data-stu-id="81550-114">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="81550-115">Windows **Me/98, windows 2000, Windows XP:** При фиксированном режиме преобразования задайте значение 1. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="81550-115">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="81550-116">редактор IME \_ кмоде \_ фуллшапе</span><span class="sxs-lookup"><span data-stu-id="81550-116">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="81550-117">Задайте значение 1, если режим полной формы; 0, если режим половинной фигуры.</span><span class="sxs-lookup"><span data-stu-id="81550-117">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="81550-118">редактор IME \_ кмоде \_ ханжаконверт</span><span class="sxs-lookup"><span data-stu-id="81550-118">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="81550-119">Задайте значение 1 в режиме преобразования ХАНДЖА. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="81550-119">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="81550-120">IME \_ кмоде \_ катакана</span><span class="sxs-lookup"><span data-stu-id="81550-120">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="81550-121">Задайте значение 1 в режиме катакана. 0, если режим хирагана.</span><span class="sxs-lookup"><span data-stu-id="81550-121">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="81550-122">\_КМОДЕ IME \_ native</span><span class="sxs-lookup"><span data-stu-id="81550-122">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="81550-123">Задайте значение 1, если собственный режим —. 0, если БУКВЕНно-цифровой режим.</span><span class="sxs-lookup"><span data-stu-id="81550-123">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="81550-124">\_КМОДЕ IME \_</span><span class="sxs-lookup"><span data-stu-id="81550-124">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="81550-125">Задайте значение 1, чтобы предотвратить обработку преобразований IME. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="81550-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="81550-126">IME \_ кмоде \_ Roman</span><span class="sxs-lookup"><span data-stu-id="81550-126">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="81550-127">Задайте значение 1 в режиме ввода ЛАТИНИЦЫ. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="81550-127">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="81550-128">редактор IME \_ кмоде \_ софткбд</span><span class="sxs-lookup"><span data-stu-id="81550-128">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="81550-129">Задайте значение 1 в режиме экранной клавиатуры. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="81550-129">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="81550-130">\_символ КМОДЕ \_ IME</span><span class="sxs-lookup"><span data-stu-id="81550-130">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="81550-131">В режиме преобразования символов задайте значение 1. 0, если нет.</span><span class="sxs-lookup"><span data-stu-id="81550-131">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="81550-132">Все остальные биты зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="81550-132">All other bits are reserved.</span></span>

 

 



