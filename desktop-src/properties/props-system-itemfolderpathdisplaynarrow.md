---
description: Понятный пользователю отображаемый путь к родительской папке элемента.
ms.assetid: f60b7465-bca4-4c7b-9caf-9cda1bf6eeeb
title: System. Итемфолдерпасдисплайнарров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898927c23aae95b5037919c908a3ae86e020e1fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080861"
---
# <a name="systemitemfolderpathdisplaynarrow"></a><span data-ttu-id="fcffe-103">System. Итемфолдерпасдисплайнарров</span><span class="sxs-lookup"><span data-stu-id="fcffe-103">System.ItemFolderPathDisplayNarrow</span></span>

<span data-ttu-id="fcffe-104">Понятный пользователю отображаемый путь к родительской папке элемента.</span><span class="sxs-lookup"><span data-stu-id="fcffe-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="fcffe-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fcffe-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplayNarrow
   shellPKey = PKEY_ItemFolderPathDisplayNarrow
   formatID = DABD30ED-0043-4789-A7F8-D013A4736622
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="fcffe-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fcffe-106">Remarks</span></span>

<span data-ttu-id="fcffe-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="fcffe-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="fcffe-108">Формат строки должен быть адаптирован таким образом, чтобы имя папки поступило в первую очередь, чтобы оптимизировать для такого столбца.</span><span class="sxs-lookup"><span data-stu-id="fcffe-108">The format of the string should be tailored so that the folder name comes first, to optimize for a narrow viewing column.</span></span> <span data-ttu-id="fcffe-109">Если папка является папкой файлов, то значение включает все локализованные имена.</span><span class="sxs-lookup"><span data-stu-id="fcffe-109">If the folder is a file folder, the value includes any localized names.</span></span> <span data-ttu-id="fcffe-110">Если [System. итемфолдерпасдисплай](./props-system-itemfolderpathdisplay.md) является VT \_ пустым, это свойство также должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="fcffe-110">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="fcffe-111">В противном случае он должен быть получен соответствующим образом источником данных из System. Итемфолдерпасдисплай.</span><span class="sxs-lookup"><span data-stu-id="fcffe-111">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcffe-112">См. также</span><span class="sxs-lookup"><span data-stu-id="fcffe-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcffe-113">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="fcffe-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="fcffe-114">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="fcffe-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="fcffe-115">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="fcffe-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="fcffe-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="fcffe-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="fcffe-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="fcffe-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="fcffe-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="fcffe-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="fcffe-119">булеанформат</span><span class="sxs-lookup"><span data-stu-id="fcffe-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="fcffe-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="fcffe-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="fcffe-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="fcffe-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="fcffe-122">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="fcffe-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="fcffe-123">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="fcffe-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="fcffe-124">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="fcffe-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="fcffe-125">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="fcffe-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="fcffe-126">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="fcffe-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
