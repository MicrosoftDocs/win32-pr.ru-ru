---
description: '\_Константы СНАТИВЕ языкового стандарта \*'
ms.assetid: 560978d7-a33c-4e62-9abd-cbd3ec38f3b5
title: Константы LOCALE_SNATIVE *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaa6942b6ed114e6cbabdb48ae55ba8f8d7bb43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272961"
---
# <a name="locale_snative-constants"></a><span data-ttu-id="5847f-103">\_Константы СНАТИВЕ языкового стандарта \*</span><span class="sxs-lookup"><span data-stu-id="5847f-103">LOCALE\_SNATIVE\* Constants</span></span>

<span data-ttu-id="5847f-104">В этом разделе определяются \_ локальные \* константы снативе, используемые NLS для представления собственных имен языков.</span><span class="sxs-lookup"><span data-stu-id="5847f-104">This topic defines the LOCALE\_SNATIVE\* constants used by NLS to represent native language names.</span></span>



| <span data-ttu-id="5847f-105">Значение</span><span class="sxs-lookup"><span data-stu-id="5847f-105">Value</span></span>                       | <span data-ttu-id="5847f-106">Значение</span><span class="sxs-lookup"><span data-stu-id="5847f-106">Meaning</span></span>                                                                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5847f-107">снативекаунтринаме ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="5847f-107">LOCALE\_SNATIVECOUNTRYNAME</span></span>  | <span data-ttu-id="5847f-108">**Windows 7 и более поздние версии:** Собственное имя страны или региона, например Espaсa for Испания.</span><span class="sxs-lookup"><span data-stu-id="5847f-108">**Windows 7 and later:** Native name of the country/region, for example, España for Spain.</span></span> <span data-ttu-id="5847f-109">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="5847f-109">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>                                                                 |
| <span data-ttu-id="5847f-110">снативектринаме ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="5847f-110">LOCALE\_SNATIVECTRYNAME</span></span>     | <span data-ttu-id="5847f-111">Не рекомендуется для Windows 7 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="5847f-111">Deprecated for Windows 7 and later.</span></span> <span data-ttu-id="5847f-112">Собственное имя страны или региона.</span><span class="sxs-lookup"><span data-stu-id="5847f-112">Native name of the country/region.</span></span> <span data-ttu-id="5847f-113">См. раздел LOCALE \_ снативекаунтринаме.</span><span class="sxs-lookup"><span data-stu-id="5847f-113">See LOCALE\_SNATIVECOUNTRYNAME.</span></span>                                                                                                                                                             |
| <span data-ttu-id="5847f-114">снативекуррнаме ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="5847f-114">LOCALE\_SNATIVECURRNAME</span></span>     | <span data-ttu-id="5847f-115">**Windows Me/98, windows 2000:** Собственное имя валюты, связанное с языковым стандартом, на родном языке языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="5847f-115">**Windows Me/98, Windows 2000:** The native name of the currency associated with the locale, in the native language of the locale.</span></span> <span data-ttu-id="5847f-116">Количество символов в этой строке не ограничено.</span><span class="sxs-lookup"><span data-stu-id="5847f-116">There is no limit on the number of characters allowed for this string.</span></span>                                                          |
| <span data-ttu-id="5847f-117">снативедигитс ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="5847f-117">LOCALE\_SNATIVEDIGITS</span></span>       | <span data-ttu-id="5847f-118">Машинные эквиваленты ASCII от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="5847f-118">Native equivalents of ASCII 0 through 9.</span></span> <span data-ttu-id="5847f-119">Максимально допустимое число символов для этой строки равно одиннадцати, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="5847f-119">The maximum number of characters allowed for this string is eleven, including a terminating null character.</span></span> <span data-ttu-id="5847f-120">Например, в арабском используется "012345 6789".</span><span class="sxs-lookup"><span data-stu-id="5847f-120">For example, Arabic uses "٠١٢٣٤٥ ٦٧٨٩".</span></span> <span data-ttu-id="5847f-121">См. также [языковой стандарт \_ идигитсубститутион](locale-idigitsubstitution.md).</span><span class="sxs-lookup"><span data-stu-id="5847f-121">See also [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md).</span></span> |
| <span data-ttu-id="5847f-122">снативедисплайнаме ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="5847f-122">LOCALE\_SNATIVEDISPLAYNAME</span></span>  | <span data-ttu-id="5847f-123">**Windows 7 и более поздние версии:** Отображаемое имя языкового стандарта на родном языке, например Deutsch (Deutschland) для немецкого языка (Германия).</span><span class="sxs-lookup"><span data-stu-id="5847f-123">**Windows 7 and later:** Display name of the locale in its native language, for example, Deutsch (Deutschland) for the locale German (Germany).</span></span> <br/>                                                                                                        |
| <span data-ttu-id="5847f-124">снативелангнаме ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="5847f-124">LOCALE\_SNATIVELANGNAME</span></span>     | <span data-ttu-id="5847f-125">Не рекомендуется для Windows 7 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="5847f-125">Deprecated for Windows 7 and later.</span></span> <span data-ttu-id="5847f-126">Собственное имя языка.</span><span class="sxs-lookup"><span data-stu-id="5847f-126">Native name of the language.</span></span> <span data-ttu-id="5847f-127">См. раздел LOCALE \_ снативелангуаженаме.</span><span class="sxs-lookup"><span data-stu-id="5847f-127">See LOCALE\_SNATIVELANGUAGENAME.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="5847f-128">снативелангуаженаме ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="5847f-128">LOCALE\_SNATIVELANGUAGENAME</span></span> | <span data-ttu-id="5847f-129">**Windows 7 и более поздние версии:** Собственное имя языка, например Հայերեն для Армянский (Армения).</span><span class="sxs-lookup"><span data-stu-id="5847f-129">**Windows 7 and later:** Native name of the language, for example, Հայերեն for Armenian (Armenia).</span></span> <span data-ttu-id="5847f-130">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="5847f-130">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>                                                         |



 

 

 




