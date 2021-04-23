---
description: Состояние зарядки устройства.
ms.assetid: 33ef8ecb-29e3-4809-9d56-8d884f9c9ff6
title: System. Devices. Чаргингстате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de306cc44900849d74ba24924c9c4066c0ffe0a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081461"
---
# <a name="systemdeviceschargingstate"></a><span data-ttu-id="478d1-103">System. Devices. Чаргингстате</span><span class="sxs-lookup"><span data-stu-id="478d1-103">System.Devices.ChargingState</span></span>

<span data-ttu-id="478d1-104">Состояние зарядки устройства.</span><span class="sxs-lookup"><span data-stu-id="478d1-104">Device charging status.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="478d1-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="478d1-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Devices.ChargingState
   shellPKey = PKEY_Devices_ChargingState
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 11
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = NotCharging
            minValue = 0
            setValue = 0
            text = Not charging
            defineToken = CHARGINGSTATE_NOT_CHARGING
         enumRange
            name = Charging
            minValue = 1
            setValue = 1
            text = Charging
            defineToken = CHARGINGSTATE_CHARGING
         enumRange
            name = UnknownChargingState
            minValue = 2
            setValue = 2
            text = Unknown charging state
            defineToken = CHARGINGSTATE_UNKNOWN_STATE
```

## <a name="remarks"></a><span data-ttu-id="478d1-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="478d1-106">Remarks</span></span>

<span data-ttu-id="478d1-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="478d1-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="478d1-108">См. также</span><span class="sxs-lookup"><span data-stu-id="478d1-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="478d1-109">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="478d1-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="478d1-110">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="478d1-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="478d1-111">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="478d1-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="478d1-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="478d1-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="478d1-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="478d1-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="478d1-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="478d1-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="478d1-115">булеанформат</span><span class="sxs-lookup"><span data-stu-id="478d1-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="478d1-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="478d1-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="478d1-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="478d1-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="478d1-118">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="478d1-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="478d1-119">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="478d1-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="478d1-120">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="478d1-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="478d1-121">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="478d1-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="478d1-122">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="478d1-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
