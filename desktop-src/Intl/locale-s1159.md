---
description: S1159 языкового стандарта \_ и \_ SAM
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 и LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b41f98ea5c07f1d88534c1e47acecfa81a4e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911671"
---
# <a name="locale_s1159-and-locale_sam"></a><span data-ttu-id="f8bb6-103">S1159 языкового стандарта \_ и \_ SAM</span><span class="sxs-lookup"><span data-stu-id="f8bb6-103">LOCALE\_S1159 and LOCALE\_SAM</span></span>

<span data-ttu-id="f8bb6-104">Строка для обозначения AM (первые 12 часов дня).</span><span class="sxs-lookup"><span data-stu-id="f8bb6-104">String for the AM designator (first 12 hours of the day).</span></span> <span data-ttu-id="f8bb6-105">Максимально допустимое число символов для этой строки, включая завершающий нуль-символ, отличается для разных выпусков Windows.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-105">The maximum number of characters allowed for this string, including a terminating null character, is different for different releases of Windows.</span></span>

<span data-ttu-id="f8bb6-106">**Windows XP:** Тринадцать, включая завершающий нуль-символ для [**сетлокалеинфо**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="f8bb6-106">**Windows XP:** Thirteen including a terminating null character for [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="f8bb6-107">Пятнадцать, включая завершающий нуль-символ для [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="f8bb6-107">Fifteen including a terminating null character for [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span></span>

<span data-ttu-id="f8bb6-108">Windows **Me/98/95, Windows NT 4,0, windows 2000:** Девять, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-108">**Windows Me/98/95, Windows NT 4.0, Windows 2000:** Nine including a terminating null character.</span></span>

<span data-ttu-id="f8bb6-109">**Windows Server 2003 и более поздние версии:** Пятнадцать, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-109">**Windows Server 2003 and later:** Fifteen including a terminating null character.</span></span>

<span data-ttu-id="f8bb6-110">Windows 10 добавил значение **\_ SAM locale** в качестве более удобного для чтения синонима для **языкового стандарта \_ S1159**.</span><span class="sxs-lookup"><span data-stu-id="f8bb6-110">Windows 10 added the value **LOCALE\_SAM** as a more readable synonym for **LOCALE\_S1159**.</span></span>

 

 



