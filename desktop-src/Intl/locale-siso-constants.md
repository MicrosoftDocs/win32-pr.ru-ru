---
description: '\_Константы SISO языкового стандарта \*'
ms.assetid: c830e9e9-b58a-4d31-929a-ed699bc08d9f
title: Константы LOCALE_SISO *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16a3d7583bc920daa2edc85b641f191b016bbbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998633"
---
# <a name="locale_siso-constants"></a><span data-ttu-id="66e73-103">\_Константы SISO языкового стандарта \*</span><span class="sxs-lookup"><span data-stu-id="66e73-103">LOCALE\_SISO\* Constants</span></span>

<span data-ttu-id="66e73-104">В этом разделе определяются \_ константы SISO локали \* , используемые NLS.</span><span class="sxs-lookup"><span data-stu-id="66e73-104">This topic defines the LOCALE\_SISO\* constants used by NLS.</span></span>



| <span data-ttu-id="66e73-105">Значение</span><span class="sxs-lookup"><span data-stu-id="66e73-105">Value</span></span>                     | <span data-ttu-id="66e73-106">Значение</span><span class="sxs-lookup"><span data-stu-id="66e73-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66e73-107">SISO3166CTRYNAME ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="66e73-107">LOCALE\_SISO3166CTRYNAME</span></span>  | <span data-ttu-id="66e73-108">**Windows Me/98, Windows NT 4,0:** Название страны или региона, основанное на стандарте ISO 3166, например "US" для США.</span><span class="sxs-lookup"><span data-stu-id="66e73-108">**Windows Me/98, Windows NT 4.0:** Country/region name, based on ISO Standard 3166, such as "US" for the United States.</span></span> <span data-ttu-id="66e73-109">Это также может возвращать число, например "029" для Карибские острова.</span><span class="sxs-lookup"><span data-stu-id="66e73-109">This can also return a number, such as "029" for Caribbean.</span></span> <span data-ttu-id="66e73-110">Максимально допустимое число символов для этой строки равно девяти, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="66e73-110">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span>                                                                                        |
| <span data-ttu-id="66e73-111">SISO3166CTRYNAME2 ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="66e73-111">LOCALE\_SISO3166CTRYNAME2</span></span> | <span data-ttu-id="66e73-112">**Windows Vista и более поздние версии:** Трехбуквенное имя региона ISO (ISO 3166 3 — код письма для страны или региона), например "США" для США.</span><span class="sxs-lookup"><span data-stu-id="66e73-112">**Windows Vista and later:** Three-letter ISO region name (ISO 3166 three-letter code for the country/region), such as "USA" for the United States.</span></span> <span data-ttu-id="66e73-113">Это также может возвращать число, например "029" для Карибские острова.</span><span class="sxs-lookup"><span data-stu-id="66e73-113">This can also return a number, such as "029" for Caribbean.</span></span> <span data-ttu-id="66e73-114">Максимально допустимое число символов для этой строки равно девяти, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="66e73-114">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span>                                                            |
| <span data-ttu-id="66e73-115">SISO639LANGNAME ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="66e73-115">LOCALE\_SISO639LANGNAME</span></span>   | <span data-ttu-id="66e73-116">**Windows Me/98, Windows NT 4,0:** Сокращенное название языка, полностью основанное на значениях стандарта ISO 639, в нижнем регистре, например en для английского языка.</span><span class="sxs-lookup"><span data-stu-id="66e73-116">**Windows Me/98, Windows NT 4.0:** The abbreviated name of the language based entirely on the ISO Standard 639 values, in lowercase form, such as "en" for English.</span></span> <span data-ttu-id="66e73-117">Это может быть трехбуквенный код для языков, у которых нет 2-буквенного кода, например "хав" для Гавайского.</span><span class="sxs-lookup"><span data-stu-id="66e73-117">This can be a 3-letter code for languages that don't have a 2-letter code, such as "haw" for Hawaiian.</span></span> <span data-ttu-id="66e73-118">Максимально допустимое число символов для этой строки равно девяти, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="66e73-118">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span> |
| <span data-ttu-id="66e73-119">SISO639LANGNAME2 ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="66e73-119">LOCALE\_SISO639LANGNAME2</span></span>  | <span data-ttu-id="66e73-120">**Windows Vista и более поздние версии:** Трехбуквенное имя языка ISO в виде строчных букв (ISO 639-2 с тремя буквами для языка), например "ENG" (английский язык).</span><span class="sxs-lookup"><span data-stu-id="66e73-120">**Windows Vista and later:** Three-letter ISO language name, in lowercase form (ISO 639-2 three-letter code for the language), such as "eng" for English.</span></span> <span data-ttu-id="66e73-121">Максимально допустимое число символов для этой строки равно девяти, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="66e73-121">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span>                                                                                                                  |



 

 

 



