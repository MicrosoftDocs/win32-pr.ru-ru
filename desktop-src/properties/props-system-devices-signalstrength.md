---
description: Сила сигнала устройства.
ms.assetid: 662d39a6-f2f5-4556-a6de-bbcc655b4adb
title: System. Devices. Сигналстренгс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901179dcf142f03ffceea14778f2763f73f16276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647669"
---
# <a name="systemdevicessignalstrength"></a><span data-ttu-id="fd559-103">System. Devices. Сигналстренгс</span><span class="sxs-lookup"><span data-stu-id="fd559-103">System.Devices.SignalStrength</span></span>

<span data-ttu-id="fd559-104">Сила сигнала устройства.</span><span class="sxs-lookup"><span data-stu-id="fd559-104">Device signal strength.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="fd559-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd559-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Devices.SignalStrength
   shellPKey = PKEY_Devices_SignalStrength
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = None
            value = 0
            text = No signal
            defineToken = SIGNALSTRENGTH_NONE
         enum
            name = Weak
            value = 1
            text = Weak signal
            defineToken = SIGNALSTRENGTH_WEAK
         enum
            name = Average
            value = 2
            text = Average signal
            defineToken = SIGNALSTRENGTH_AVERAGE
         enum
            name = Strong
            value = 3
            text = Strong signal
            defineToken = SIGNALSTRENGTH_STRONG
         enum
            name = Excellent
            value = 4
            text = Excellent signal
            defineToken = SIGNALSTRENGTH_EXCELLENT
```

## <a name="remarks"></a><span data-ttu-id="fd559-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd559-106">Remarks</span></span>

<span data-ttu-id="fd559-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="fd559-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd559-108">См. также</span><span class="sxs-lookup"><span data-stu-id="fd559-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd559-109">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="fd559-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="fd559-110">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="fd559-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="fd559-111">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="fd559-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="fd559-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="fd559-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="fd559-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="fd559-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="fd559-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="fd559-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="fd559-115">булеанформат</span><span class="sxs-lookup"><span data-stu-id="fd559-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="fd559-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="fd559-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="fd559-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="fd559-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="fd559-118">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="fd559-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="fd559-119">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="fd559-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="fd559-120">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="fd559-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="fd559-121">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="fd559-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="fd559-122">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="fd559-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
