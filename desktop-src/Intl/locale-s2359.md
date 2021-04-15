---
description: ЯЗЫКовой стандарт \_ S2359 и \_ SPM locale
ms.assetid: 8a97073e-84f6-47d9-98fb-65760e8a6cd8
title: LOCALE_S2359 и LOCALE_SPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0c22d541102fcdf0826778de591dc4100dda55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683964"
---
# <a name="locale_s2359-and-locale_spm"></a><span data-ttu-id="b772f-103">ЯЗЫКовой стандарт \_ S2359 и \_ SPM locale</span><span class="sxs-lookup"><span data-stu-id="b772f-103">LOCALE\_S2359 and LOCALE\_SPM</span></span>

<span data-ttu-id="b772f-104">Строка для обозначения PM (второй 12-часовой день).</span><span class="sxs-lookup"><span data-stu-id="b772f-104">String for the PM designator (second 12 hours of the day).</span></span> <span data-ttu-id="b772f-105">Максимально допустимое число символов для этой строки различается для разных выпусков Windows.</span><span class="sxs-lookup"><span data-stu-id="b772f-105">The maximum number of characters allowed for this string is different for different releases of Windows.</span></span>

<span data-ttu-id="b772f-106">**Windows XP:** Тринадцать, включая завершающий нуль-символ для [**сетлокалеинфо**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="b772f-106">**Windows XP:** Thirteen including a terminating null character for [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="b772f-107">Пятнадцать, включая завершающий нуль-символ для [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="b772f-107">Fifteen including a terminating null character for [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span></span>

<span data-ttu-id="b772f-108">Windows **Me/98/95, Windows NT 4,0, windows 2000:** Девять, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="b772f-108">**Windows Me/98/95, Windows NT 4.0, Windows 2000:** Nine including a terminating null character.</span></span>

<span data-ttu-id="b772f-109">**Windows Server 2003 и более поздние версии:** Пятнадцать, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="b772f-109">**Windows Server 2003 and later:** Fifteen including a terminating null character.</span></span>

<span data-ttu-id="b772f-110">В Windows 10 добавлен параметр **locale \_ SPM** в качестве более удобного синонима для **\_ S2359 локали**.</span><span class="sxs-lookup"><span data-stu-id="b772f-110">Windows 10 added the value **LOCALE\_SPM** as a more readable synonym for **LOCALE\_S2359**.</span></span>

 

 



