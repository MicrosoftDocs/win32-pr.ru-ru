---
description: 'Префикс элемента, используемый для сообщений электронной почты, в которых тема начинается с префикса &\# 0034; Re: &\# 0034;.'
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System. Итемнамепрефикс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf669dd867c8cf60046f226e33dae18f46060cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991317"
---
# <a name="systemitemnameprefix"></a><span data-ttu-id="31998-103">System. Итемнамепрефикс</span><span class="sxs-lookup"><span data-stu-id="31998-103">System.ItemNamePrefix</span></span>

<span data-ttu-id="31998-104">Префикс элемента, используемый для сообщений электронной почты, в которых тема начинается с префикса "Re:".</span><span class="sxs-lookup"><span data-stu-id="31998-104">The prefix of an item, used for e-mail messages where the subject begins with the prefix "Re:".</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="31998-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31998-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="31998-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31998-106">Remarks</span></span>

<span data-ttu-id="31998-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="31998-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="31998-108">Если элемент является файлом, значение этого свойства — VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="31998-108">If the item is a file, then the value of this property is VT\_EMPTY.</span></span> <span data-ttu-id="31998-109">Если элемент является сообщением, то значением этого свойства являются префиксы перенаправления или отклика (включая двоеточие, но без пробелов) или VT \_ Empty, если префикс отсутствует.</span><span class="sxs-lookup"><span data-stu-id="31998-109">If the item is a message, then the value of this property is the forwarding or reply prefixes (including the delimiting colon, but no whitespace), or VT\_EMPTY if there is no prefix.</span></span>

<span data-ttu-id="31998-110">Примеры значений</span><span class="sxs-lookup"><span data-stu-id="31998-110">Example values:</span></span>



| <span data-ttu-id="31998-111">System. Итемнамепрефикс</span><span class="sxs-lookup"><span data-stu-id="31998-111">System.ItemNamePrefix</span></span> | <span data-ttu-id="31998-112">System. ItemName</span><span class="sxs-lookup"><span data-stu-id="31998-112">System.ItemName</span></span>  | <span data-ttu-id="31998-113">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="31998-113">System.ItemNameDisplay</span></span> |
|-----------------------|------------------|------------------------|
| <span data-ttu-id="31998-114">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="31998-114">VT\_EMPTY</span></span>             | <span data-ttu-id="31998-115">"Отличный день"</span><span class="sxs-lookup"><span data-stu-id="31998-115">"Great day"</span></span>      | <span data-ttu-id="31998-116">"Отличный день"</span><span class="sxs-lookup"><span data-stu-id="31998-116">"Great day"</span></span>            |
| <span data-ttu-id="31998-117">"Re:"</span><span class="sxs-lookup"><span data-stu-id="31998-117">"Re:"</span></span>                 | <span data-ttu-id="31998-118">"Отличный день"</span><span class="sxs-lookup"><span data-stu-id="31998-118">"Great day"</span></span>      | <span data-ttu-id="31998-119">"Re: отличный день"</span><span class="sxs-lookup"><span data-stu-id="31998-119">"Re: Great day"</span></span>        |
| <span data-ttu-id="31998-120">"ФВД:"</span><span class="sxs-lookup"><span data-stu-id="31998-120">"Fwd: "</span></span>               | <span data-ttu-id="31998-121">"Месячный бюджет"</span><span class="sxs-lookup"><span data-stu-id="31998-121">"Monthly budget"</span></span> | <span data-ttu-id="31998-122">"ФВД: месячный бюджет"</span><span class="sxs-lookup"><span data-stu-id="31998-122">"Fwd: Monthly budget"</span></span>  |
| <span data-ttu-id="31998-123">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="31998-123">VT\_EMPTY</span></span>             | <span data-ttu-id="31998-124">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="31998-124">accounts.xls</span></span>     | <span data-ttu-id="31998-125">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="31998-125">accounts.xls</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="31998-126">См. также</span><span class="sxs-lookup"><span data-stu-id="31998-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31998-127">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="31998-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="31998-128">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="31998-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="31998-129">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="31998-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="31998-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="31998-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="31998-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="31998-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="31998-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="31998-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="31998-133">булеанформат</span><span class="sxs-lookup"><span data-stu-id="31998-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="31998-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="31998-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="31998-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="31998-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="31998-136">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="31998-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="31998-137">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="31998-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="31998-138">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="31998-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="31998-139">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="31998-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="31998-140">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="31998-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
