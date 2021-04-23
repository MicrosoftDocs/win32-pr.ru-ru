---
description: Заголовок элемента.
ms.assetid: 8fb948d6-2677-4e5d-b283-8757c3df574d
title: System.Title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee57037a35c08fd3a6be4f4a0ce7a8475f82cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703065"
---
# <a name="systemtitle"></a><span data-ttu-id="4b581-103">System.Title</span><span class="sxs-lookup"><span data-stu-id="4b581-103">System.Title</span></span>

<span data-ttu-id="4b581-104">Заголовок элемента.</span><span class="sxs-lookup"><span data-stu-id="4b581-104">The title of the item.</span></span> <span data-ttu-id="4b581-105">Например, заголовок документа, тема сообщения, подпись к фотографии или название музыкальной композиции.</span><span class="sxs-lookup"><span data-stu-id="4b581-105">For example, the title of a document, the subject of a message, the caption of a photo, or the name of a music track.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="4b581-106">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b581-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Title
   shellPKey = PKEY_Title
   formatID = F29F85E0-4FF9-1068-AB91-08002B27B3D9
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
```

## <a name="remarks"></a><span data-ttu-id="4b581-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b581-107">Remarks</span></span>

<span data-ttu-id="4b581-108">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="4b581-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="4b581-109">Это свойство сопоставляется с *заголовком* свойства OLE Document.</span><span class="sxs-lookup"><span data-stu-id="4b581-109">This property maps to the OLE document property *Title*.</span></span> <span data-ttu-id="4b581-110">[System. Title]() — это часто используемое свойство, особенно в разнородных списках элементов, где элементы могут иметь множество различных типов.</span><span class="sxs-lookup"><span data-stu-id="4b581-110">[System.Title]() is a commonly used property, particularly in heterogeneous lists of items where the items can be of many different types.</span></span> <span data-ttu-id="4b581-111">Поэтому рекомендуется, чтобы обработчики свойств заполнили это свойство, даже если оно избыточно. Например, сообщение электронной почты, которое заполняет как System. Title, так и [System. subject](./props-system-subject.md) тем же значением.</span><span class="sxs-lookup"><span data-stu-id="4b581-111">Therefore, it is recommended that property handlers populate this property even if it is redundant; for example, an e-mail, which would populate both System.Title and [System.Subject](./props-system-subject.md) with the same value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b581-112">См. также</span><span class="sxs-lookup"><span data-stu-id="4b581-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b581-113">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="4b581-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="4b581-114">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="4b581-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="4b581-115">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="4b581-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="4b581-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="4b581-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="4b581-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4b581-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="4b581-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="4b581-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="4b581-119">булеанформат</span><span class="sxs-lookup"><span data-stu-id="4b581-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="4b581-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="4b581-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="4b581-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4b581-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="4b581-122">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="4b581-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="4b581-123">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="4b581-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="4b581-124">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="4b581-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="4b581-125">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="4b581-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="4b581-126">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="4b581-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
