---
description: Определяет, зашифрован ли элемент.
ms.assetid: fd93f915-6af3-4bde-982e-6774a1ca83af
title: System. с шифрованием
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05f6f1d31838f885820938e9be38ef161c168ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647317"
---
# <a name="systemisencrypted"></a><span data-ttu-id="5ed6d-103">System. с шифрованием</span><span class="sxs-lookup"><span data-stu-id="5ed6d-103">System.IsEncrypted</span></span>

<span data-ttu-id="5ed6d-104">Определяет, зашифрован ли элемент.</span><span class="sxs-lookup"><span data-stu-id="5ed6d-104">Identifies whether the item is encrypted.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="5ed6d-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="5ed6d-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.IsEncrypted
   shellPKey = PKEY_IsEncrypted
   formatID = 90E5E14E-648B-4826-B2AA-ACAF790E3513
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Encrypted
            value = #TRUE#
            text = Encrypted
            defineToken = ISENCRYPTED_ENCRYPTED
         enum
            name = NotEncrypted
            value = #FALSE#
            text = Unencrypted
            defineToken = ISENCRYPTED_NOTENCRYPTED
```

## <a name="windows-vista"></a><span data-ttu-id="5ed6d-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ed6d-106">Windows Vista</span></span>

```
propertyDescription
   name = System.IsEncrypted
   shellPKey = PKEY_IsEncrypted
   formatID = 90E5E14E-648B-4826-B2AA-ACAF790E3513
   propID = 10
   SearchInfo
      IsColumn = true
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            value = #TRUE#
            text = Encrypted
            mnemonics = encrypted
         enum
            value = #FALSE#
            text = Unencrypted
            mnemonics = unencrypted
```

## <a name="remarks"></a><span data-ttu-id="5ed6d-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ed6d-107">Remarks</span></span>

<span data-ttu-id="5ed6d-108">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="5ed6d-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="5ed6d-109">Это свойство было введено в выпуске Windows Search 4,0.</span><span class="sxs-lookup"><span data-stu-id="5ed6d-109">This property was introduced with the release of Windows Search 4.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ed6d-110">См. также</span><span class="sxs-lookup"><span data-stu-id="5ed6d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ed6d-111">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="5ed6d-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-112">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="5ed6d-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-113">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="5ed6d-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="5ed6d-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="5ed6d-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="5ed6d-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-117">булеанформат</span><span class="sxs-lookup"><span data-stu-id="5ed6d-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="5ed6d-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5ed6d-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-120">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="5ed6d-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-121">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="5ed6d-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-122">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="5ed6d-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-123">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="5ed6d-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="5ed6d-124">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="5ed6d-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
