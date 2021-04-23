---
description: сшортдате ЛОКАЛи \_
ms.assetid: 55333a53-1205-42eb-aa1a-c248c52a8a3f
title: LOCALE_SSHORTDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15077b4466fd74c02dd53bd7324aceba9233cc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683015"
---
# <a name="locale_sshortdate"></a><span data-ttu-id="bb431-103">сшортдате ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="bb431-103">LOCALE\_SSHORTDATE</span></span>

<span data-ttu-id="bb431-104">Краткая строка форматирования даты для языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="bb431-104">Short date formatting string for the locale.</span></span> <span data-ttu-id="bb431-105">Максимально допустимое число символов для этой строки — 80, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="bb431-105">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="bb431-106">Строка может состоять из комбинаций [изображений "день", "месяц", "год" и "формат эры](day--month--year--and-era-format-pictures.md)".</span><span class="sxs-lookup"><span data-stu-id="bb431-106">The string can consist of a combination of [day, month, year, and era format pictures](day--month--year--and-era-format-pictures.md).</span></span> <span data-ttu-id="bb431-107">Например, "M/d/гггг" означает, что 3 сентября 2004 записал 9/3/2004.</span><span class="sxs-lookup"><span data-stu-id="bb431-107">For example, "M/d/yyyy" indicates that September 3, 2004 is written 9/3/2004.</span></span>

<span data-ttu-id="bb431-108">Языковые стандарты могут определять несколько кратких форматов даты.</span><span class="sxs-lookup"><span data-stu-id="bb431-108">Locales can define multiple short date formats.</span></span> <span data-ttu-id="bb431-109">Чтобы получить все краткие форматы даты для этого языкового стандарта, используйте [енумдатеформатс](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [енумдатеформатсекс](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)или [енумдатеформатсексекс](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span><span class="sxs-lookup"><span data-stu-id="bb431-109">To get all of the short date formats for this locale, use [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa), or [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).</span></span>

 

 



