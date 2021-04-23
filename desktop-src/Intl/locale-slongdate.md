---
description: слонгдате ЛОКАЛи \_
ms.assetid: 1b72cd57-819e-4b1f-bbb0-b600a9e8631c
title: LOCALE_SLONGDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503b24d81318f471b33a4ab644a059607e5ac490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154531"
---
# <a name="locale_slongdate"></a><span data-ttu-id="1df29-103">слонгдате ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="1df29-103">LOCALE\_SLONGDATE</span></span>

<span data-ttu-id="1df29-104">Строка длинного форматирования даты для языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="1df29-104">Long date formatting string for the locale.</span></span> <span data-ttu-id="1df29-105">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="1df29-105">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="1df29-106">Строка может состоять из [рисунков в формате "день", "месяц", "год" и "формат эры](day--month--year--and-era-format-pictures.md) " и любой строки символов, заключенной в одинарные кавычки.</span><span class="sxs-lookup"><span data-stu-id="1df29-106">The string can consist of a combination of [day, month, year, and era format pictures](day--month--year--and-era-format-pictures.md) and any string of characters enclosed in single quotes.</span></span> <span data-ttu-id="1df29-107">Символы в одинарных кавычках остаются в указанном виде.</span><span class="sxs-lookup"><span data-stu-id="1df29-107">Characters in single quotes remain as specified.</span></span> <span data-ttu-id="1df29-108">Например, в качестве даты в испанском (Испания) используется формат "dddd, дд" de "MMMM" de "гггг".</span><span class="sxs-lookup"><span data-stu-id="1df29-108">For example, the Spanish (Spain) long date is "dddd, dd' de 'MMMM' de 'yyyy".</span></span> <span data-ttu-id="1df29-109">В языковых стандартах можно определить несколько длинных форматов даты.</span><span class="sxs-lookup"><span data-stu-id="1df29-109">Locales can define multiple long date formats.</span></span>

<span data-ttu-id="1df29-110">Чтобы получить полный формат даты для языкового стандарта, используйте [енумдатеформатс](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [енумдатеформатсекс](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)или [енумдатеформатсексекс](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span><span class="sxs-lookup"><span data-stu-id="1df29-110">To get all of the long date formats for a locale, use [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa), or [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span></span>

 

 



