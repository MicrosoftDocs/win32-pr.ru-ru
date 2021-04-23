---
description: Указывает, является ли устройство перемещаемым.
ms.assetid: d2382e96-7ca4-42e4-8e5b-89f1da736904
title: System. Devices. роуминг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482bb306eeeed03592ae18bb7a8f63c109f2f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103909911"
---
# <a name="systemdevicesroaming"></a><span data-ttu-id="6b7c9-103">System. Devices. роуминг</span><span class="sxs-lookup"><span data-stu-id="6b7c9-103">System.Devices.Roaming</span></span>

<span data-ttu-id="6b7c9-104">Указывает, является ли устройство перемещаемым.</span><span class="sxs-lookup"><span data-stu-id="6b7c9-104">Indicates whether the device is roaming.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="6b7c9-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="6b7c9-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Devices.Roaming
   shellPKey = PKEY_Devices_Roaming
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = NotRoaming
            minValue = 0
            setValue = 0
            text = Not roaming
            defineToken = ROAMING_NOT_ROAMING
         enumRange
            name = Roaming
            minValue = 1
            setValue = 1
            text = Roaming
            defineToken = ROAMING_ROAMING
         enumRange
            name = UnknownStatus
            minValue = 2
            setValue = 2
            text = Unknown roaming status
            defineToken = ROAMING_UNKNOWN_STATUS
```

## <a name="remarks"></a><span data-ttu-id="6b7c9-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b7c9-106">Remarks</span></span>

<span data-ttu-id="6b7c9-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="6b7c9-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b7c9-108">См. также</span><span class="sxs-lookup"><span data-stu-id="6b7c9-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b7c9-109">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="6b7c9-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-110">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="6b7c9-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-111">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="6b7c9-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="6b7c9-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6b7c9-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6b7c9-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-115">булеанформат</span><span class="sxs-lookup"><span data-stu-id="6b7c9-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="6b7c9-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6b7c9-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-118">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="6b7c9-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-119">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="6b7c9-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-120">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="6b7c9-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-121">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="6b7c9-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6b7c9-122">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="6b7c9-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
