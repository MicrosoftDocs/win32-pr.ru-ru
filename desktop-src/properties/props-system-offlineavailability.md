---
description: .
ms.assetid: 4d0c880b-923d-4f83-91da-dd99bf111f13
title: System. Оффлинеаваилабилити
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca82f7e8da4454be8a5e9dd557ff63a7784dc8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998344"
---
# <a name="systemofflineavailability"></a><span data-ttu-id="946de-103">System. Оффлинеаваилабилити</span><span class="sxs-lookup"><span data-stu-id="946de-103">System.OfflineAvailability</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="946de-104">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="946de-104">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.OfflineAvailability
   shellPKey = PKEY_OfflineAvailability
   formatID = A94688B6-7D9F-4570-A648-E3DFC0AB2B3F
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotAvailable
            value = 0
            text = Online-only
            defineToken = OFFLINEAVAILABILITY_NOT_AVAILABLE
         enum
            name = Available
            value = 1
            text = Available
            defineToken = OFFLINEAVAILABILITY_AVAILABLE
         enum
            name = AlwaysAvailable
            value = 2
            text = Available offline
            defineToken = OFFLINEAVAILABILITY_ALWAYS_AVAILABLE
```

## <a name="windows-8-windows-7"></a><span data-ttu-id="946de-105">Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="946de-105">Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.OfflineAvailability
   shellPKey = PKEY_OfflineAvailability
   formatID = A94688B6-7D9F-4570-A648-E3DFC0AB2B3F
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotAvailable
            value = 0
            text = Not available
            defineToken = OFFLINEAVAILABILITY_NOT_AVAILABLE
         enum
            name = Available
            value = 1
            text = Available
            defineToken = OFFLINEAVAILABILITY_AVAILABLE
         enum
            name = AlwaysAvailable
            value = 2
            text = Always available
            defineToken = OFFLINEAVAILABILITY_ALWAYS_AVAILABLE
```

## <a name="windows-vista"></a><span data-ttu-id="946de-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="946de-106">Windows Vista</span></span>

```
propertyDescription
   name = System.OfflineAvailability
   shellPKey = PKEY_OfflineAvailability
   formatID = A94688B6-7D9F-4570-A648-E3DFC0AB2B3F
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Not available
            defineName = OFFLINEAVAILABILITY_NOT_AVAILABLE
         enum
            value = 1
            text = Available
            defineName = OFFLINEAVAILABILITY_AVAILABLE
         enum
            value = 2
            text = Always available
            defineName = OFFLINEAVAILABILITY_ALWAYS_AVAILABLE
```

## <a name="remarks"></a><span data-ttu-id="946de-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="946de-107">Remarks</span></span>

<span data-ttu-id="946de-108">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="946de-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="946de-109">См. также</span><span class="sxs-lookup"><span data-stu-id="946de-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="946de-110">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="946de-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="946de-111">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="946de-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="946de-112">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="946de-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="946de-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="946de-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="946de-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="946de-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="946de-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="946de-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="946de-116">булеанформат</span><span class="sxs-lookup"><span data-stu-id="946de-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="946de-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="946de-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="946de-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="946de-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="946de-119">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="946de-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="946de-120">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="946de-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="946de-121">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="946de-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="946de-122">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="946de-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="946de-123">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="946de-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
