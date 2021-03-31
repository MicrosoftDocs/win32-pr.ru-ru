---
description: Оставшийся срок работы аккумулятора устройства и его состояние зарядки.
ms.assetid: 9c6800ed-ca55-4202-8dfb-6e430121d6b7
title: System.Devices.BatТериплусчаргинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f249b65afe57b1e9959bd180f7bd3dc9342c85f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264567"
---
# <a name="systemdevicesbatterypluscharging"></a><span data-ttu-id="58eba-103">System.Devices.BatТериплусчаргинг</span><span class="sxs-lookup"><span data-stu-id="58eba-103">System.Devices.BatteryPlusCharging</span></span>

<span data-ttu-id="58eba-104">Оставшийся срок работы аккумулятора устройства и его состояние зарядки.</span><span class="sxs-lookup"><span data-stu-id="58eba-104">Remaining battery life of the device and its charging state.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="58eba-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="58eba-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Devices.BatteryPlusCharging
   shellPKey = PKEY_Devices_BatteryPlusCharging
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 22
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = CriticallyLow
            minValue = 0
            setValue = 5
            text = Critically low battery
            defineToken = BATTERYPLUSCHARGING_CRITICALLY_LOW
         enumRange
            name = Low
            minValue = 11
            setValue = 18
            text = Low battery
            defineToken = BATTERYPLUSCHARGING_LOW
         enumRange
            name = Average
            minValue = 26
            setValue = 60
            text = Average battery
            defineToken = BATTERYPLUSCHARGING_AVERAGE
         enumRange
            name = Full
            minValue = 90
            setValue = 95
            text = Full battery
            defineToken = BATTERYPLUSCHARGING_FULL
         enumRange
            name = CriticallyLow
            minValue = 101
            setValue = 5
            text = Critically low battery (charging)
            defineToken = BATTERYPLUSCHARGING_CHARGING_CRITICALLY_LOW
         enumRange
            name = Low
            minValue = 111
            setValue = 18
            text = Low battery (charging)
            defineToken = BATTERYPLUSCHARGING_CHARGING_LOW
         enumRange
            name = Average
            minValue = 126
            setValue = 60
            text = Average battery (charging)
            defineToken = BATTERYPLUSCHARGING_CHARGING_AVERAGE
         enumRange
            name = Full
            minValue = 190
            setValue = 95
            text = Full battery (charging)
            defineToken = BATTERYPLUSCHARGING_CHARGING_FULL
         enumRange
            name = UnknownStatus
            minValue = 201
            setValue = 201
            text = Unknown battery and charging status
            defineToken = BATTERYPLUSCHARGING_UNKNOWN_STATUS
```

## <a name="remarks"></a><span data-ttu-id="58eba-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58eba-106">Remarks</span></span>

<span data-ttu-id="58eba-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="58eba-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58eba-108">См. также</span><span class="sxs-lookup"><span data-stu-id="58eba-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58eba-109">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="58eba-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="58eba-110">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="58eba-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="58eba-111">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="58eba-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="58eba-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="58eba-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="58eba-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="58eba-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="58eba-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="58eba-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="58eba-115">булеанформат</span><span class="sxs-lookup"><span data-stu-id="58eba-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="58eba-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="58eba-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="58eba-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="58eba-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="58eba-118">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="58eba-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="58eba-119">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="58eba-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="58eba-120">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="58eba-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="58eba-121">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="58eba-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="58eba-122">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="58eba-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
