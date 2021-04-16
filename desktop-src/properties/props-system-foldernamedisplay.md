---
description: Это свойство похоже на System. Итемнамедисплай, за исключением того, что оно задается только для папок, для файлов, которые она будет пустой.
ms.assetid: 4517a4bf-3cc1-4835-b21b-03de5b33db0c
title: System. Фолдернамедисплай
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60922054e80a6589bcb04c3962a4527ee62eaf7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650919"
---
# <a name="systemfoldernamedisplay"></a><span data-ttu-id="8b1f6-103">System. Фолдернамедисплай</span><span class="sxs-lookup"><span data-stu-id="8b1f6-103">System.FolderNameDisplay</span></span>

<span data-ttu-id="8b1f6-104">Это свойство похоже на System. Итемнамедисплай, за исключением того, что оно задается только для папок, для файлов, которые она будет пустой.</span><span class="sxs-lookup"><span data-stu-id="8b1f6-104">This property is similar to System.ItemNameDisplay except it is only set for folders, for files it will be empty.</span></span> <span data-ttu-id="8b1f6-105">Это полезно для разделения файлов и папок, используя его в качестве первого ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="8b1f6-105">This is useful to segregate files and folders by using this as the first sort key.</span></span> <span data-ttu-id="8b1f6-106">Если System. Итемдате используется в качестве второго ключа сортировки, он формирует результаты с папками, предварительно упорядоченными по имени, а затем по датам.</span><span class="sxs-lookup"><span data-stu-id="8b1f6-106">When System.ItemDate is used as a second sort key it produces results with folders first ordered by name, then files ordered by date.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="8b1f6-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8b1f6-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.FolderNameDisplay
   shellPKey = PKEY_FolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 25
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="8b1f6-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b1f6-108">Remarks</span></span>

<span data-ttu-id="8b1f6-109">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="8b1f6-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b1f6-110">См. также</span><span class="sxs-lookup"><span data-stu-id="8b1f6-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b1f6-111">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="8b1f6-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-112">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="8b1f6-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-113">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="8b1f6-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="8b1f6-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="8b1f6-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="8b1f6-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-117">булеанформат</span><span class="sxs-lookup"><span data-stu-id="8b1f6-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="8b1f6-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="8b1f6-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-120">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="8b1f6-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-121">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="8b1f6-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-122">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="8b1f6-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-123">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="8b1f6-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="8b1f6-124">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="8b1f6-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
