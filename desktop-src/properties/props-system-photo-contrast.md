---
description: Указывает направление обработки контрастности, применяемой камерой при создании образа. &\#0034; 0&\# 0034; указывает &\# 0034; Обычная&\# 0034;; &\# 0034; 1&\# 0034; указывает &\# 0034; Soft&\# 0034;; &\# 0034; 2&\# 0034; указывает &\# 0034; Жесткий&\# 0034;.
ms.assetid: 32f89149-b90d-4fe9-9d1a-b8bb966d62fe
title: System. photo. контраст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4117f13d35a352971a5f9b9f8685816f8ffbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647312"
---
# <a name="systemphotocontrast"></a><span data-ttu-id="bbb7b-104">System. photo. контраст</span><span class="sxs-lookup"><span data-stu-id="bbb7b-104">System.Photo.Contrast</span></span>

<span data-ttu-id="bbb7b-105">Указывает направление обработки контрастности, применяемой камерой при создании образа.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-105">Indicates the direction of contrast processing applied by the camera when the image was taken.</span></span> <span data-ttu-id="bbb7b-106">"0" означает "нормальный"; "1" означает "Soft"; "2" означает "жесткое".</span><span class="sxs-lookup"><span data-stu-id="bbb7b-106">"0" indicates "Normal"; "1" indicates "Soft"; "2" indicates "Hard".</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="bbb7b-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbb7b-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.Contrast
   shellPKey = PKEY_Photo_Contrast
   formatID = 2A785BA9-8D23-4DED-82E6-60A350C86A10
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 0
            text = Normal
            defineToken = PHOTO_CONTRAST_NORMAL
         enum
            name = Soft
            value = 1
            text = Soft
            defineToken = PHOTO_CONTRAST_SOFT
         enum
            name = Hard
            value = 2
            text = Hard
            defineToken = PHOTO_CONTRAST_HARD
```

## <a name="windows-vista"></a><span data-ttu-id="bbb7b-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbb7b-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Contrast
   shellPKey = PKEY_Photo_Contrast
   formatID = 2A785BA9-8D23-4DED-82E6-60A350C86A10
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Normal
            defineName = PHOTO_CONTRAST_NORMAL
         enum
            value = 1
            text = Soft
            defineName = PHOTO_CONTRAST_SOFT
         enum
            value = 2
            text = Hard
            defineName = PHOTO_CONTRAST_HARD
```

## <a name="remarks"></a><span data-ttu-id="bbb7b-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbb7b-109">Remarks</span></span>

<span data-ttu-id="bbb7b-110">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbb7b-111">См. также</span><span class="sxs-lookup"><span data-stu-id="bbb7b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbb7b-112">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="bbb7b-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-113">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="bbb7b-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-114">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="bbb7b-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="bbb7b-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="bbb7b-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="bbb7b-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-118">булеанформат</span><span class="sxs-lookup"><span data-stu-id="bbb7b-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="bbb7b-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="bbb7b-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-121">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="bbb7b-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-122">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="bbb7b-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-123">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="bbb7b-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-124">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="bbb7b-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="bbb7b-125">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="bbb7b-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
