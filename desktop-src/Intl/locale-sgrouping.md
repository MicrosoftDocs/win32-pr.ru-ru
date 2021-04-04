---
description: сграупинг ЛОКАЛи \_
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7242f7d515ce17872376b9a067a7b41831a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999767"
---
# <a name="locale_sgrouping"></a><span data-ttu-id="296ab-103">сграупинг ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="296ab-103">LOCALE\_SGROUPING</span></span>

<span data-ttu-id="296ab-104">Размеры для каждой группы цифр слева от десятичного разделителя.</span><span class="sxs-lookup"><span data-stu-id="296ab-104">Sizes for each group of digits to the left of the decimal.</span></span> <span data-ttu-id="296ab-105">Максимально допустимое число символов для этой строки равно десяти, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="296ab-105">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="296ab-106">Для каждой группы требуется явный размер, а размеры разделяются точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="296ab-106">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="296ab-107">Если Последнее значение равно 0, предыдущее значение повторяется.</span><span class="sxs-lookup"><span data-stu-id="296ab-107">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="296ab-108">Например, чтобы сгруппировать тысячи, укажите значение 3; 0.</span><span class="sxs-lookup"><span data-stu-id="296ab-108">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="296ab-109">Индийские национальные стандарты группируют первые тысячи и затем группируются по сотням.</span><span class="sxs-lookup"><span data-stu-id="296ab-109">Indic locales group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="296ab-110">Например, 12, 34, 56789 представляется 3; 2; 0.</span><span class="sxs-lookup"><span data-stu-id="296ab-110">For example, 12,34,56,789 is represented by 3;2;0.</span></span>

<span data-ttu-id="296ab-111">Дополнительные примеры:</span><span class="sxs-lookup"><span data-stu-id="296ab-111">Further examples:</span></span>



| <span data-ttu-id="296ab-112">Спецификация</span><span class="sxs-lookup"><span data-stu-id="296ab-112">Specification</span></span> | <span data-ttu-id="296ab-113">Результирующая строка</span><span class="sxs-lookup"><span data-stu-id="296ab-113">Resulting string</span></span>   |
|---------------|--------------------|
| <span data-ttu-id="296ab-114">3; 0</span><span class="sxs-lookup"><span data-stu-id="296ab-114">3;0</span></span>           | <span data-ttu-id="296ab-115">3 000 000 000 000</span><span class="sxs-lookup"><span data-stu-id="296ab-115">3,000,000,000,000</span></span>  |
| <span data-ttu-id="296ab-116">3; 2; 0</span><span class="sxs-lookup"><span data-stu-id="296ab-116">3;2;0</span></span>         | <span data-ttu-id="296ab-117">30, 00, 00, 00, 00000</span><span class="sxs-lookup"><span data-stu-id="296ab-117">30,00,00,00,00,000</span></span> |
| <span data-ttu-id="296ab-118">3</span><span class="sxs-lookup"><span data-stu-id="296ab-118">3</span></span>             | <span data-ttu-id="296ab-119">3 000 000 000 000</span><span class="sxs-lookup"><span data-stu-id="296ab-119">3000000000,000</span></span>     |
| <span data-ttu-id="296ab-120">3; 2</span><span class="sxs-lookup"><span data-stu-id="296ab-120">3;2</span></span>           | <span data-ttu-id="296ab-121">30000000, 00000</span><span class="sxs-lookup"><span data-stu-id="296ab-121">30000000,00,000</span></span>    |



 

 

 



