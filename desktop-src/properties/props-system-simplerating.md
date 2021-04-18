---
description: Система оценок, использующая диапазон целочисленных значений от 0 до 5.
ms.assetid: 50353ba9-86dd-4172-91b4-1898c8fc5522
title: System. Симплератинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4741edd076b6027bc5f8dfbe3b2ff2a31374a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712826"
---
# <a name="systemsimplerating"></a><span data-ttu-id="6e11c-103">System. Симплератинг</span><span class="sxs-lookup"><span data-stu-id="6e11c-103">System.SimpleRating</span></span>

<span data-ttu-id="6e11c-104">Система оценок, использующая диапазон целочисленных значений от 0 до 5.</span><span class="sxs-lookup"><span data-stu-id="6e11c-104">A rating system that uses a range of integer values between 0 and 5.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="6e11c-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e11c-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.SimpleRating
   shellPKey = PKEY_SimpleRating
   formatID = A09F084E-AD41-489F-8076-AA5BE3082BCA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="6e11c-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e11c-106">Remarks</span></span>

<span data-ttu-id="6e11c-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="6e11c-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="6e11c-108">Для совместимости с системой оценки оболочки Windows Vista обработчик свойств также должен заполнить свойство [System. рейтингов](./props-system-rating.md) с сопоставлением, как описано для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="6e11c-108">For compatibility with the Windows Vista Shell rating system, your property handler should also populate the [System.Rating](./props-system-rating.md) property with the mapping as described for that property.</span></span>

<span data-ttu-id="6e11c-109">Используйте следующую таблицу для преобразования из [System. рейтингов](./props-system-rating.md) в [System. симплератинг]().</span><span class="sxs-lookup"><span data-stu-id="6e11c-109">Use the following table to convert from [System.Rating](./props-system-rating.md) to [System.SimpleRating]().</span></span>



| <span data-ttu-id="6e11c-110">System. Оценка</span><span class="sxs-lookup"><span data-stu-id="6e11c-110">System.Rating</span></span> | <span data-ttu-id="6e11c-111">System. Симплератинг</span><span class="sxs-lookup"><span data-stu-id="6e11c-111">System.SimpleRating</span></span> |
|---------------|---------------------|
| <span data-ttu-id="6e11c-112">0</span><span class="sxs-lookup"><span data-stu-id="6e11c-112">0</span></span>             | <span data-ttu-id="6e11c-113">0</span><span class="sxs-lookup"><span data-stu-id="6e11c-113">0</span></span>                   |
| <span data-ttu-id="6e11c-114">1–12</span><span class="sxs-lookup"><span data-stu-id="6e11c-114">1-12</span></span>          | <span data-ttu-id="6e11c-115">1</span><span class="sxs-lookup"><span data-stu-id="6e11c-115">1</span></span>                   |
| <span data-ttu-id="6e11c-116">13-37</span><span class="sxs-lookup"><span data-stu-id="6e11c-116">13-37</span></span>         | <span data-ttu-id="6e11c-117">2</span><span class="sxs-lookup"><span data-stu-id="6e11c-117">2</span></span>                   |
| <span data-ttu-id="6e11c-118">38-62</span><span class="sxs-lookup"><span data-stu-id="6e11c-118">38-62</span></span>         | <span data-ttu-id="6e11c-119">3</span><span class="sxs-lookup"><span data-stu-id="6e11c-119">3</span></span>                   |
| <span data-ttu-id="6e11c-120">63-87</span><span class="sxs-lookup"><span data-stu-id="6e11c-120">63-87</span></span>         | <span data-ttu-id="6e11c-121">4</span><span class="sxs-lookup"><span data-stu-id="6e11c-121">4</span></span>                   |
| <span data-ttu-id="6e11c-122">88-99</span><span class="sxs-lookup"><span data-stu-id="6e11c-122">88-99</span></span>         | <span data-ttu-id="6e11c-123">5</span><span class="sxs-lookup"><span data-stu-id="6e11c-123">5</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="6e11c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="6e11c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e11c-125">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="6e11c-125">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6e11c-126">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="6e11c-126">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6e11c-127">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="6e11c-127">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6e11c-128">typeInfo</span><span class="sxs-lookup"><span data-stu-id="6e11c-128">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6e11c-129">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6e11c-129">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6e11c-130">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6e11c-130">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6e11c-131">булеанформат</span><span class="sxs-lookup"><span data-stu-id="6e11c-131">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6e11c-132">numberFormat</span><span class="sxs-lookup"><span data-stu-id="6e11c-132">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6e11c-133">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6e11c-133">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6e11c-134">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="6e11c-134">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6e11c-135">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="6e11c-135">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6e11c-136">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="6e11c-136">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6e11c-137">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="6e11c-137">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6e11c-138">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="6e11c-138">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
