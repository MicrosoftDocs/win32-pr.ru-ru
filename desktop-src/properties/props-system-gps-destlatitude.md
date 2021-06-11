---
description: Узнайте, как свойство System. GPS. Дестлатитуде указывает широту точки назначения.
ms.assetid: 63d8a3a3-76ec-4121-b48b-eb5034117d04
title: System. GPS. Дестлатитуде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbed51e89926b8bb505457bd9fd7bf7bd3b69ff2
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988969"
---
# <a name="systemgpsdestlatitude"></a><span data-ttu-id="774cc-103">System. GPS. Дестлатитуде</span><span class="sxs-lookup"><span data-stu-id="774cc-103">System.GPS.DestLatitude</span></span>

<span data-ttu-id="774cc-104">Указывает широту точки назначения.</span><span class="sxs-lookup"><span data-stu-id="774cc-104">Indicates the latitude of the destination point.</span></span> <span data-ttu-id="774cc-105">Это массив из трех значений, как показано ниже: индекс 0 — это градусы, индекс 1 — минуты, индекс 2 — секунды.</span><span class="sxs-lookup"><span data-stu-id="774cc-105">This is an array of three values, as follows: index 0 is the degrees, index 1 is the minutes, index 2 is the seconds.</span></span> <span data-ttu-id="774cc-106">Каждый из них вычисляется на основе значений в списке PKEY \_ GPS \_ ДЕСТЛАТИТУДЕНУМЕРАТОР и PKEY \_ GPS \_ дестлатитудеденоминатор.</span><span class="sxs-lookup"><span data-stu-id="774cc-106">Each is calculated from the values in PKEY\_GPS\_DestLatitudeNumerator and PKEY\_GPS\_DestLatitudeDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="774cc-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="774cc-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.GPS.DestLatitude
   shellPKey = PKEY_GPS_DestLatitude
   formatID = 9D1D7CC5-5C39-451C-86B3-928E2D18CC47
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="774cc-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="774cc-108">Remarks</span></span>

<span data-ttu-id="774cc-109">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="774cc-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="774cc-110">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="774cc-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="774cc-111">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="774cc-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="774cc-112">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="774cc-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="774cc-113">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="774cc-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="774cc-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="774cc-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="774cc-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="774cc-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="774cc-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="774cc-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="774cc-117">булеанформат</span><span class="sxs-lookup"><span data-stu-id="774cc-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="774cc-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="774cc-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="774cc-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="774cc-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="774cc-120">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="774cc-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="774cc-121">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="774cc-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="774cc-122">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="774cc-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="774cc-123">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="774cc-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="774cc-124">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="774cc-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
