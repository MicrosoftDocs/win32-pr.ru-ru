---
description: Для этой строки должна быть задана фонетическая версия отображаемого имени, определенная в System. Итемнамедисплай в языковых стандартах CJK (CHS пиньинь, JPN хирагана, KOR хангыль и т. д.).
ms.assetid: eb491644-bf59-4439-9e9b-bcafde619d66
title: System. Итемнамесортоверриде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79f9bb07eb15eb5d25fbfa1e95d4c0f80b35611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265691"
---
# <a name="systemitemnamesortoverride"></a><span data-ttu-id="a0762-103">System. Итемнамесортоверриде</span><span class="sxs-lookup"><span data-stu-id="a0762-103">System.ItemNameSortOverride</span></span>

<span data-ttu-id="a0762-104">Для этой строки должна быть задана фонетическая версия отображаемого имени, определенная в System. Итемнамедисплай в языковых стандартах CJK (CHS пиньинь, JPN хирагана, KOR хангыль и т. д.).</span><span class="sxs-lookup"><span data-stu-id="a0762-104">This string should be set to the phonetic version of the display name as defined in System.ItemNameDisplay in CJK locales(CHS Pinyin, JPN Hiragana, KOR Hangul, etc.).</span></span> <span data-ttu-id="a0762-105">Первый символ этого поля также используется для группирования имен по фирстлеттер.</span><span class="sxs-lookup"><span data-stu-id="a0762-105">The first character of this field is also used for grouping names by firstletter.</span></span> <span data-ttu-id="a0762-106">Для большинства языков, отличных от CJK, это поле задавать не нужно (в этом случае будет использоваться System. Итемнамедисплай). Однако если желательно переопределить букву группировки (например, чтобы удалить ведущие статьи, например "a" и "The"), здесь можно указать альтернативную строку.</span><span class="sxs-lookup"><span data-stu-id="a0762-106">For most non-CJK languages, this field does not need to be set (in which case System.ItemNameDisplay will be used).However, if it is desirable to override the grouping letter (for example, to remove leading articles such as "a" and "the"),an alternate string can be provided here.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="a0762-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="a0762-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.ItemNameSortOverride
   shellPKey = PKEY_ItemNameSortOverride
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="a0762-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0762-108">Remarks</span></span>

<span data-ttu-id="a0762-109">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="a0762-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0762-110">См. также</span><span class="sxs-lookup"><span data-stu-id="a0762-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0762-111">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="a0762-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a0762-112">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="a0762-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a0762-113">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="a0762-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a0762-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="a0762-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a0762-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a0762-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a0762-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a0762-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a0762-117">булеанформат</span><span class="sxs-lookup"><span data-stu-id="a0762-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a0762-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="a0762-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a0762-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a0762-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a0762-120">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="a0762-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a0762-121">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="a0762-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a0762-122">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="a0762-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a0762-123">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="a0762-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a0762-124">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="a0762-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
