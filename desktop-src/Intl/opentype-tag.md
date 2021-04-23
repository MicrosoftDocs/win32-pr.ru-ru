---
description: Определяет 4-байтовый массив, который содержит 4 8-разрядные значения ASCII для пробелов, A – Z или a – z для определения тегов в скриптах, языках и шрифтах OpenType.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf973c03f26bdb8f8b3799e1780fed5075d315cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683098"
---
# <a name="opentype_tag"></a><span data-ttu-id="82666-103">\_тег OPENTYPE</span><span class="sxs-lookup"><span data-stu-id="82666-103">OPENTYPE\_TAG</span></span>

<span data-ttu-id="82666-104">Определяет 4-байтовый массив, который содержит 4 8-разрядные значения ASCII для пробелов, A – Z или a – z для определения тегов в скриптах, языках и шрифтах OpenType.</span><span class="sxs-lookup"><span data-stu-id="82666-104">Defines a 4-byte array that contains four 8-bit ASCII values of space, A-Z, or a-z to identify OpenType script, language, and font feature tags.</span></span>


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a><span data-ttu-id="82666-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82666-105">Remarks</span></span>

<span data-ttu-id="82666-106">В следующих примерах определяются представления тегов функций OpenType.</span><span class="sxs-lookup"><span data-stu-id="82666-106">The following examples define representations of OpenType feature tags.</span></span>

-   <span data-ttu-id="82666-107">Тег функции для функции лигатуры — "Лига".</span><span class="sxs-lookup"><span data-stu-id="82666-107">The feature tag for the ligature feature is "liga".</span></span>
-   <span data-ttu-id="82666-108">Теги языка для румынского, урду и фарси имеют «ROM», «УРД» и «FAR» соответственно.</span><span class="sxs-lookup"><span data-stu-id="82666-108">The language tags for Romanian, Urdu, and Persian are "ROM ", "URD ", and "FAR ", respectively.</span></span> <span data-ttu-id="82666-109">Обратите внимание, что каждый из этих тегов заканчивается пробелом.</span><span class="sxs-lookup"><span data-stu-id="82666-109">Note that each of these tags ends with a space.</span></span>
-   <span data-ttu-id="82666-110">Теги script для латиницы и арабского алфавита — это «ЛАТН» и «Арабская» соответственно.</span><span class="sxs-lookup"><span data-stu-id="82666-110">The script tags for Latin and Arabic scripts are "latn" and "arab", respectively.</span></span>

<span data-ttu-id="82666-111">Дополнительные сведения о тегах функций OpenType и спецификации OpenType см. в разделе <https://www.microsoft.com/typography/otspec/featuretags.htm> .</span><span class="sxs-lookup"><span data-stu-id="82666-111">For more information on OpenType feature tags and the OpenType specification, see <https://www.microsoft.com/typography/otspec/featuretags.htm>.</span></span>

## <a name="requirements"></a><span data-ttu-id="82666-112">Требования</span><span class="sxs-lookup"><span data-stu-id="82666-112">Requirements</span></span>



| <span data-ttu-id="82666-113">Требование</span><span class="sxs-lookup"><span data-stu-id="82666-113">Requirement</span></span> | <span data-ttu-id="82666-114">Значение</span><span class="sxs-lookup"><span data-stu-id="82666-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82666-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82666-115">Minimum supported client</span></span><br/> | <span data-ttu-id="82666-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82666-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="82666-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82666-117">Minimum supported server</span></span><br/> | <span data-ttu-id="82666-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82666-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="82666-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="82666-119">Redistributable</span></span><br/>          | <span data-ttu-id="82666-120">Usp10.dll версии 1,600 или более поздней в Windows.</span><span class="sxs-lookup"><span data-stu-id="82666-120">Usp10.dll version 1.600 or greater onWindows XPand later</span></span><br/>                |
| <span data-ttu-id="82666-121">Header</span><span class="sxs-lookup"><span data-stu-id="82666-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="82666-122"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="82666-122"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82666-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82666-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82666-124">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="82666-124">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="82666-125">Структуры Uniscribe</span><span class="sxs-lookup"><span data-stu-id="82666-125">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="82666-126">**скриптжетфонталтернатеглифс**</span><span class="sxs-lookup"><span data-stu-id="82666-126">**ScriptGetFontAlternateGlyphs**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[<span data-ttu-id="82666-127">**скриптжетфонтфеатуретагс**</span><span class="sxs-lookup"><span data-stu-id="82666-127">**ScriptGetFontFeatureTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[<span data-ttu-id="82666-128">**скриптжетфонтлангуажетагс**</span><span class="sxs-lookup"><span data-stu-id="82666-128">**ScriptGetFontLanguageTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[<span data-ttu-id="82666-129">**скриптжетфонтскрипттагс**</span><span class="sxs-lookup"><span data-stu-id="82666-129">**ScriptGetFontScriptTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[<span data-ttu-id="82666-130">**скриптитемизеопентипе**</span><span class="sxs-lookup"><span data-stu-id="82666-130">**ScriptItemizeOpenType**</span></span>](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[<span data-ttu-id="82666-131">**скриптплацеопентипе**</span><span class="sxs-lookup"><span data-stu-id="82666-131">**ScriptPlaceOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[<span data-ttu-id="82666-132">**скриптпоситионсинглеглиф**</span><span class="sxs-lookup"><span data-stu-id="82666-132">**ScriptPositionSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[<span data-ttu-id="82666-133">**скриптшапеопентипе**</span><span class="sxs-lookup"><span data-stu-id="82666-133">**ScriptShapeOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[<span data-ttu-id="82666-134">**скриптсубститутесинглеглиф**</span><span class="sxs-lookup"><span data-stu-id="82666-134">**ScriptSubstituteSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




