---
description: Раздел реестра EUDC содержит один или несколько подразделов, содержащих значения, определяющие шрифты, связанные с определяемыми пользователем символами (Еудкс) для данной кодовой страницы.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781f7c28460c2e56f4bcdb393277f509f88a0383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664317"
---
# <a name="eudc"></a><span data-ttu-id="aa45d-103">EUDC</span><span class="sxs-lookup"><span data-stu-id="aa45d-103">EUDC</span></span>

<span data-ttu-id="aa45d-104">Раздел реестра EUDC содержит один или несколько подразделов, содержащих значения, определяющие шрифты, связанные с [определяемыми пользователем символами (еудкс)](end-user-defined-characters.md) для данной кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="aa45d-104">The EUDC registry key contains one or more subkeys containing values defining the fonts associated with [end-user-defined characters (EUDCs)](end-user-defined-characters.md) for a given code page.</span></span> <span data-ttu-id="aa45d-105">Он имеет следующее расположение в реестре:</span><span class="sxs-lookup"><span data-stu-id="aa45d-105">It has the following registry location:</span></span>

<span data-ttu-id="aa45d-106">HKEY \_ текущий \_ пользователь \\ EUDC</span><span class="sxs-lookup"><span data-stu-id="aa45d-106">HKEY\_CURRENT\_USER\\EUDC</span></span>

<span data-ttu-id="aa45d-107">Формат будет следующим:</span><span class="sxs-lookup"><span data-stu-id="aa45d-107">The format is:</span></span>

<span data-ttu-id="aa45d-108">EUDC Системдефаултеудкфонт = Труетипиудкфонтфиленаме Труетипефонттипефаце = Труетипиудкфонтфиленаме</span><span class="sxs-lookup"><span data-stu-id="aa45d-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span></span>

<span data-ttu-id="aa45d-109">где:</span><span class="sxs-lookup"><span data-stu-id="aa45d-109">where:</span></span>



|                          |                                                                                                                                          |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa45d-110">системдефаултеудкфонт</span><span class="sxs-lookup"><span data-stu-id="aa45d-110">SystemDefaultEUDCFont</span></span>    | <span data-ttu-id="aa45d-111">Предопределенное имя, используемое для задания системного шрифта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aa45d-111">Predefined name used to set the system default font.</span></span> <span data-ttu-id="aa45d-112">Отсутствует системный шрифт EUDC по умолчанию, если эта запись не указана явно.</span><span class="sxs-lookup"><span data-stu-id="aa45d-112">There is no system default EUDC font unless this entry is explicitly specified.</span></span>     |
| <span data-ttu-id="aa45d-113">труетипефонттипефаце</span><span class="sxs-lookup"><span data-stu-id="aa45d-113">TrueTypeFontTypeface</span></span>     | <span data-ttu-id="aa45d-114">Определяемое пользователем имя, связанное с шрифтом non-EUDC TrueType.</span><span class="sxs-lookup"><span data-stu-id="aa45d-114">User-defined name associated with a non-EUDC TrueType font.</span></span>                                                                              |
| <span data-ttu-id="aa45d-115">труетипиудкфонтфиленаме</span><span class="sxs-lookup"><span data-stu-id="aa45d-115">TrueTypeEUDCFontFileName</span></span> | <span data-ttu-id="aa45d-116">Строка, состоящая из имени файла отдельного файла шрифта EUDC.</span><span class="sxs-lookup"><span data-stu-id="aa45d-116">String consisting of the file name of a separate EUDC font file.</span></span> <span data-ttu-id="aa45d-117">Этот файл определяет шрифт, который будет связан с Труетипефонттипефаце.</span><span class="sxs-lookup"><span data-stu-id="aa45d-117">This file identifies a font to be associated with TrueTypeFontTypeface.</span></span> |



 

<span data-ttu-id="aa45d-118">В следующем примере показан ключ EUDC для кодовой страницы 932.</span><span class="sxs-lookup"><span data-stu-id="aa45d-118">The following example shows the EUDC key for code page 932.</span></span>


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



<span data-ttu-id="aa45d-119">В следующем примере для системного шрифта EUDC по умолчанию задается значение EUDC. ttf и связывается отдельные шрифты EUDC Минеудк. ttf и Готеудк. ttf с названиями шрифтов MS Минчо и MS Gothic соответственно.</span><span class="sxs-lookup"><span data-stu-id="aa45d-119">The following example sets the system default EUDC font to be Eudc.ttf and associates the separate EUDC fonts Mineudc.ttf and Goteudc.ttf with the font names MS Mincho and MS Gothic, respectively.</span></span>


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



<span data-ttu-id="aa45d-120">Когда кодовая страница Windows (System ACP), связанная с языком для программ, не поддерживающих Юникод, соответствует подразделу, подсистема GDI выполняет поиск пар "подраздел-значение", чтобы получить отображаемые сведения об этом символе.</span><span class="sxs-lookup"><span data-stu-id="aa45d-120">When the Windows code page (system ACP) associated with the language for non-Unicode programs matches the subkey, the GDI subsystem looks to the subkey value pairs to obtain display information about the character.</span></span> <span data-ttu-id="aa45d-121">Сначала он ищет имя, совпадающее с текущим шрифтом.</span><span class="sxs-lookup"><span data-stu-id="aa45d-121">It first looks for a name matching the current font.</span></span> <span data-ttu-id="aa45d-122">Если таковые отсутствуют, он проверяет значение Системдефаултеудкфонт.</span><span class="sxs-lookup"><span data-stu-id="aa45d-122">If there is none, it examines the SystemDefaultEUDCFont value.</span></span> <span data-ttu-id="aa45d-123">Если значение не определено, GDI обрабатывает символ как неопределенный.</span><span class="sxs-lookup"><span data-stu-id="aa45d-123">If no value is defined, GDI treats the character as undefined.</span></span>

<span data-ttu-id="aa45d-124">Обратите внимание, что сам текст не обязательно должен находиться в кодовой странице Windows.</span><span class="sxs-lookup"><span data-stu-id="aa45d-124">Note that the text itself does not have to be in the Windows code page.</span></span> <span data-ttu-id="aa45d-125">Например, предположим, что кодовая страница содержит идентификатор 1252, кодовую страницу Windows по умолчанию для английского языка.</span><span class="sxs-lookup"><span data-stu-id="aa45d-125">For example, assume that the code page has the identifier 1252, the default Windows code page for English.</span></span> <span data-ttu-id="aa45d-126">Приложение передает одну кодовую точку Юникода U + E000 в закрытой области использования Юникода (PUA) в [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="aa45d-126">An application passes the single Unicode code point U+E000, in the Unicode private use area (PUA), to [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="aa45d-127">В этом случае GDI просматривает значения реестра в разделе 1252, чтобы получить сведения о шрифтах для свойств отображаемого символа.</span><span class="sxs-lookup"><span data-stu-id="aa45d-127">In this case, GDI looks at the registry values under 1252 to obtain the font information for the character display properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa45d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="aa45d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa45d-129">Записи реестра EUDC</span><span class="sxs-lookup"><span data-stu-id="aa45d-129">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="aa45d-130">еудккодеранже</span><span class="sxs-lookup"><span data-stu-id="aa45d-130">EUDCCodeRange</span></span>](eudccoderange.md)
</dt> </dl>

 

 
