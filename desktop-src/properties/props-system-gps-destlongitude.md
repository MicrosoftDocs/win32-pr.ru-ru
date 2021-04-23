---
description: Указывает широту точки назначения.
ms.assetid: 72a3fb10-4554-4a4d-bb73-ee515341b9c1
title: System. GPS. Дестлонгитуде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e11cb93fece8b5d2d95c649bdaf87c01390a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647326"
---
# <a name="systemgpsdestlongitude"></a><span data-ttu-id="05a0d-103">System. GPS. Дестлонгитуде</span><span class="sxs-lookup"><span data-stu-id="05a0d-103">System.GPS.DestLongitude</span></span>

<span data-ttu-id="05a0d-104">Указывает широту точки назначения.</span><span class="sxs-lookup"><span data-stu-id="05a0d-104">Indicates the latitude of the destination point.</span></span> <span data-ttu-id="05a0d-105">Это массив из трех значений, как показано ниже: индекс 0 — это градусы, индекс 1 — минуты, индекс 2 — секунды.</span><span class="sxs-lookup"><span data-stu-id="05a0d-105">This is an array of three values, as follows: index 0 is the degrees, index 1 is the minutes, index 2 is the seconds.</span></span> <span data-ttu-id="05a0d-106">Каждый из них вычисляется на основе значений в списке PKEY \_ GPS \_ ДЕСТЛОНГИТУДЕНУМЕРАТОР и PKEY \_ GPS \_ дестлонгитудеденоминатор.</span><span class="sxs-lookup"><span data-stu-id="05a0d-106">Each is calculated from the values in PKEY\_GPS\_DestLongitudeNumerator and PKEY\_GPS\_DestLongitudeDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="05a0d-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05a0d-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.GPS.DestLongitude
   shellPKey = PKEY_GPS_DestLongitude
   formatID = 47A96261-CB4C-4807-8AD3-40B9D9DBC6BC
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="05a0d-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05a0d-108">Remarks</span></span>

<span data-ttu-id="05a0d-109">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="05a0d-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05a0d-110">См. также</span><span class="sxs-lookup"><span data-stu-id="05a0d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05a0d-111">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="05a0d-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="05a0d-112">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="05a0d-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="05a0d-113">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="05a0d-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="05a0d-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="05a0d-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="05a0d-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="05a0d-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="05a0d-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="05a0d-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="05a0d-117">булеанформат</span><span class="sxs-lookup"><span data-stu-id="05a0d-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="05a0d-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="05a0d-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="05a0d-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="05a0d-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="05a0d-120">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="05a0d-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="05a0d-121">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="05a0d-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="05a0d-122">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="05a0d-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="05a0d-123">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="05a0d-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="05a0d-124">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="05a0d-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
