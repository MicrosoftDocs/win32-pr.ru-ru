---
description: NULL указывает на нормальный случай (файл доступен в автономном режиме). Частичный вариант относится только к папкам, в которых некоторое содержимое может быть доступно в автономном режиме, а некоторые — нет.
ms.assetid: 46b03632-702e-46df-8204-33ada85adbee
title: System. Филеоффлинеаваилабилитистатус
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ca5c3f004c89cfb7b8625f9eb939a42f7fe842
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910176"
---
# <a name="systemfileofflineavailabilitystatus"></a><span data-ttu-id="a0c0f-104">System. Филеоффлинеаваилабилитистатус</span><span class="sxs-lookup"><span data-stu-id="a0c0f-104">System.FileOfflineAvailabilityStatus</span></span>

<span data-ttu-id="a0c0f-105">NULL указывает на нормальный случай (файл доступен в автономном режиме).</span><span class="sxs-lookup"><span data-stu-id="a0c0f-105">Null indicates the normal case (file is available offline).</span></span> <span data-ttu-id="a0c0f-106">Частичный вариант относится только к папкам, в которых некоторое содержимое может быть доступно в автономном режиме, а некоторые — нет.</span><span class="sxs-lookup"><span data-stu-id="a0c0f-106">The partial case is only for folders where some content may be available offline and some may not.</span></span>

## <a name="windows-10-version-1703"></a><span data-ttu-id="a0c0f-107">Windows 10 версии 1703</span><span class="sxs-lookup"><span data-stu-id="a0c0f-107">Windows 10, version 1703</span></span>

```
propertyDescription
   name = System.FileOfflineAvailabilityStatus
   shellPKey = PKEY_FileOfflineAvailabilityStatus
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotAvailableOffline
            value = 0
            text = NotAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_NOTAVAILABLEOFFLINE
         enum
            name = PartiallyAvailableOffline
            value = 1
            text = PartiallyAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_PARTIAL
         enum
            name = Complete
            value = 2
            text = Complete
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_COMPLETE
         enum
            name = CompletePinned
            value = 3
            text = CompletePinned
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_COMPLETE_PINNED
         enum
            name = Excluded
            value = 4
            text = Excluded
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_EXCLUDED
         enum
            name = Empty
            value = 5
            text = Empty
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_FOLDER_EMPTY
```

## <a name="windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="a0c0f-108">Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a0c0f-108">Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.FileOfflineAvailabilityStatus
   shellPKey = PKEY_FileOfflineAvailabilityStatus
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotAvailableOffline
            value = 0
            text = NotAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_PROP_NOTAVAILABLEOFFLINE
         enum
            name = PartiallyAvailableOffline
            value = 1
            text = PartiallyAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_PROP_PARTIALLYAVAILABLEOFFLINE
```

## <a name="remarks"></a><span data-ttu-id="a0c0f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0c0f-109">Remarks</span></span>

<span data-ttu-id="a0c0f-110">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="a0c0f-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0c0f-111">См. также</span><span class="sxs-lookup"><span data-stu-id="a0c0f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0c0f-112">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="a0c0f-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-113">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="a0c0f-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-114">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="a0c0f-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="a0c0f-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a0c0f-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a0c0f-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-118">булеанформат</span><span class="sxs-lookup"><span data-stu-id="a0c0f-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="a0c0f-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a0c0f-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-121">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="a0c0f-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-122">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="a0c0f-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-123">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="a0c0f-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-124">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="a0c0f-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a0c0f-125">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="a0c0f-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
