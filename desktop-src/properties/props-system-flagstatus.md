---
description: 'Состояние флага. Значения: (0 = None 1 = белый 2 = red).'
ms.assetid: 0485deab-2408-4147-acaa-cb09e9e0032a
title: System. Флагстатус
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dde42493f2d450854c3f53de5ecab26394f0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264281"
---
# <a name="systemflagstatus"></a><span data-ttu-id="efcfb-104">System. Флагстатус</span><span class="sxs-lookup"><span data-stu-id="efcfb-104">System.FlagStatus</span></span>

<span data-ttu-id="efcfb-105">Состояние флага.</span><span class="sxs-lookup"><span data-stu-id="efcfb-105">The status of a flag.</span></span> <span data-ttu-id="efcfb-106">Значения: (0 = None 1 = белый 2 = red).</span><span class="sxs-lookup"><span data-stu-id="efcfb-106">Values: (0=none 1=white 2=Red).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="efcfb-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="efcfb-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.FlagStatus
   shellPKey = PKEY_FlagStatus
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Int32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotFlagged
            value = 0
            text = Not flagged
            defineToken = FLAGSTATUS_NOTFLAGGED
            mnemonics = Unflagged
         enum
            name = Completed
            value = 1
            text = Completed
            defineToken = FLAGSTATUS_COMPLETED
         enum
            name = FollowUp
            value = 2
            text = Follow Up
            defineToken = FLAGSTATUS_FOLLOWUP
            mnemonics = Followup Flag|followup|follow
```

## <a name="windows-vista"></a><span data-ttu-id="efcfb-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="efcfb-108">Windows Vista</span></span>

```
propertyDescription
   name = System.FlagStatus
   shellPKey = PKEY_FlagStatus
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 12
   SearchInfo
      IsColumn = true
   typeInfo
      type = Int32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Not flagged
            defineName = FLAGSTATUS_NOTFLAGGED
            mnemonics = Unflagged
         enum
            value = 1
            text = Completed
            defineName = FLAGSTATUS_COMPLETED
         enum
            value = 2
            text = Follow Up
            defineName = FLAGSTATUS_FOLLOWUP
            mnemonics = Followup Flag|followup|follow
```

## <a name="remarks"></a><span data-ttu-id="efcfb-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efcfb-109">Remarks</span></span>

<span data-ttu-id="efcfb-110">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="efcfb-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efcfb-111">См. также</span><span class="sxs-lookup"><span data-stu-id="efcfb-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efcfb-112">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="efcfb-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="efcfb-113">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="efcfb-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="efcfb-114">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="efcfb-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="efcfb-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="efcfb-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="efcfb-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="efcfb-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="efcfb-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="efcfb-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="efcfb-118">булеанформат</span><span class="sxs-lookup"><span data-stu-id="efcfb-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="efcfb-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="efcfb-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="efcfb-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="efcfb-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="efcfb-121">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="efcfb-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="efcfb-122">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="efcfb-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="efcfb-123">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="efcfb-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="efcfb-124">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="efcfb-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="efcfb-125">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="efcfb-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
