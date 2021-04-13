---
description: Понятное пользователю отображаемое имя родительской папки элемента.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. Итемфолдернамедисплай
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265475"
---
# <a name="systemitemfoldernamedisplay"></a><span data-ttu-id="59e0d-103">System. Итемфолдернамедисплай</span><span class="sxs-lookup"><span data-stu-id="59e0d-103">System.ItemFolderNameDisplay</span></span>

<span data-ttu-id="59e0d-104">Понятное пользователю отображаемое имя родительской папки элемента.</span><span class="sxs-lookup"><span data-stu-id="59e0d-104">The user-friendly display name of an item's parent folder.</span></span>

<span data-ttu-id="59e0d-105">Это является производным от [System. итемфолдерпасдисплай](./props-system-itemfolderpathdisplay.md).</span><span class="sxs-lookup"><span data-stu-id="59e0d-105">This is derived from [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md).</span></span> <span data-ttu-id="59e0d-106">Если это свойство имеет значение VT \_ Empty, это свойство также должно быть.</span><span class="sxs-lookup"><span data-stu-id="59e0d-106">If that property is VT\_EMPTY, then this property should be too.</span></span>

<span data-ttu-id="59e0d-107">Если папка является папкой файлов, значение будет локализовано, если локализованное имя доступно.</span><span class="sxs-lookup"><span data-stu-id="59e0d-107">If the folder is a file folder, the value will be localized if a localized name is available.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="59e0d-108">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59e0d-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="59e0d-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59e0d-109">Remarks</span></span>

<span data-ttu-id="59e0d-110">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="59e0d-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="59e0d-111">Если [System. итемфолдерпасдисплай](./props-system-itemfolderpathdisplay.md) является VT \_ пустым, это свойство также должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="59e0d-111">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="59e0d-112">В противном случае он должен быть получен соответствующим образом источником данных из System. Итемфолдерпасдисплай.</span><span class="sxs-lookup"><span data-stu-id="59e0d-112">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

<span data-ttu-id="59e0d-113">Примеры:</span><span class="sxs-lookup"><span data-stu-id="59e0d-113">Examples:</span></span>



| <span data-ttu-id="59e0d-114">Заданный путь</span><span class="sxs-lookup"><span data-stu-id="59e0d-114">Given path</span></span>                             | <span data-ttu-id="59e0d-115">Отображаемое имя папки</span><span class="sxs-lookup"><span data-stu-id="59e0d-115">Folder Display Name</span></span> |
|----------------------------------------|---------------------|
| <span data-ttu-id="59e0d-116">c: \\ мифилес \\ Text \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="59e0d-116">c:\\MyFiles\\Text\\hello.txt</span></span>           | <span data-ttu-id="59e0d-117">Текст</span><span class="sxs-lookup"><span data-stu-id="59e0d-117">Text</span></span>                |
| <span data-ttu-id="59e0d-118">\\\\\\Общая папка сервера \\ MyDir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="59e0d-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="59e0d-119">MyDir</span><span class="sxs-lookup"><span data-stu-id="59e0d-119">mydir</span></span>               |
| <span data-ttu-id="59e0d-120">\\\\\\Общая папка сервера \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="59e0d-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="59e0d-121">поделиться</span><span class="sxs-lookup"><span data-stu-id="59e0d-121">share</span></span>               |
| <span data-ttu-id="59e0d-122">c: \\ папки \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="59e0d-122">c:\\Folders\\MyFolder</span></span>                  | <span data-ttu-id="59e0d-123">Папки</span><span class="sxs-lookup"><span data-stu-id="59e0d-123">Folders</span></span>             |
| <span data-ttu-id="59e0d-124">Учетная запись/маилбокс/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="59e0d-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="59e0d-125">Папка "Входящие"</span><span class="sxs-lookup"><span data-stu-id="59e0d-125">Inbox</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="59e0d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="59e0d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59e0d-127">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="59e0d-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="59e0d-128">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="59e0d-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="59e0d-129">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="59e0d-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="59e0d-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="59e0d-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="59e0d-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="59e0d-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="59e0d-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="59e0d-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="59e0d-133">булеанформат</span><span class="sxs-lookup"><span data-stu-id="59e0d-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="59e0d-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="59e0d-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="59e0d-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="59e0d-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="59e0d-136">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="59e0d-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="59e0d-137">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="59e0d-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="59e0d-138">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="59e0d-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="59e0d-139">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="59e0d-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="59e0d-140">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="59e0d-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
