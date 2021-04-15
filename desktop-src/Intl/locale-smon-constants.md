---
description: '\_Константы СМОН языкового стандарта \*'
ms.assetid: df7f026b-2f2d-420f-8a14-656734409835
title: Константы LOCALE_SMON *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932888360cc81e08a1cff1f45082b5fc1b91ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662715"
---
# <a name="locale_smon-constants"></a><span data-ttu-id="ed5f6-103">\_Константы СМОН языкового стандарта \*</span><span class="sxs-lookup"><span data-stu-id="ed5f6-103">LOCALE\_SMON\* Constants</span></span>

<span data-ttu-id="ed5f6-104">В этом разделе определяются \_ локальные \* константы смон, используемые NLS в представлениях денежных значений.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-104">This topic defines the LOCALE\_SMON\* constants used by NLS in representing monetary values.</span></span>



| <span data-ttu-id="ed5f6-105">Значение</span><span class="sxs-lookup"><span data-stu-id="ed5f6-105">Value</span></span>                   | <span data-ttu-id="ed5f6-106">Значение</span><span class="sxs-lookup"><span data-stu-id="ed5f6-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed5f6-107">смондеЦималсеп ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="ed5f6-107">LOCALE\_SMONDECIMALSEP</span></span>  | <span data-ttu-id="ed5f6-108">Символы, используемые в качестве десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-108">Character(s) used as the monetary decimal separator.</span></span> <span data-ttu-id="ed5f6-109">Максимально допустимое число символов для этой строки равно четырем, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-109">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="ed5f6-110">Например, если денежная сумма отображается как "$3,40", так же как "три доллара и 40 центов" отображается в США, десятичный разделитель ".".</span><span class="sxs-lookup"><span data-stu-id="ed5f6-110">For example, if a monetary amount is displayed as "$3.40", just as "three dollars and forty cents" is displayed in the United States, then the monetary decimal separator is ".".</span></span>                                                                                                                                             |
| <span data-ttu-id="ed5f6-111">смонграупинг ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="ed5f6-111">LOCALE\_SMONGROUPING</span></span>    | <span data-ttu-id="ed5f6-112">Размеры для каждой группы денежных знаков, слева от десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-112">Sizes for each group of monetary digits to the left of the decimal.</span></span> <span data-ttu-id="ed5f6-113">Максимально допустимое число символов для этой строки равно десяти, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-113">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="ed5f6-114">Для каждой группы требуется явный размер, а размеры разделяются точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-114">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="ed5f6-115">Если Последнее значение равно 0, предыдущее значение повторяется.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-115">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="ed5f6-116">Например, чтобы сгруппировать тысячи, укажите значение 3; 0.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-116">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="ed5f6-117">Индийские языки группируют первые тысячи, а затем группируются по сотням.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-117">Indic languages group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="ed5f6-118">Например, 12, 34, 56789 представляется 3; 2; 0.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-118">For example 12,34,56,789 is represented by 3;2;0.</span></span> |
| <span data-ttu-id="ed5f6-119">смонсаусандсеп ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="ed5f6-119">LOCALE\_SMONTHOUSANDSEP</span></span> | <span data-ttu-id="ed5f6-120">Символы, используемые как разделитель денежных знаков между группами цифр слева от десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-120">Character(s) used as the monetary separator between groups of digits to the left of the decimal.</span></span> <span data-ttu-id="ed5f6-121">Максимально допустимое число символов для этой строки равно четырем, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-121">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="ed5f6-122">Как правило, группы представляют тысячи.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-122">Typically, the groups represent thousands.</span></span> <span data-ttu-id="ed5f6-123">Однако в зависимости от значения, указанного для параметра LOCALE \_ смонграупинг, они могут представлять что-то другое.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-123">However, depending on the value specified for LOCALE\_SMONGROUPING, they can represent something else.</span></span>                                                                                                                                 |



 

 

 



