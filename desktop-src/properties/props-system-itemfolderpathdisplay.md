---
description: Понятный пользователю отображаемый путь к родительской папке элемента.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System. Итемфолдерпасдисплай
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4ae4c9178356d36c644f1bc886d63331155e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711877"
---
# <a name="systemitemfolderpathdisplay"></a><span data-ttu-id="aecd8-103">System. Итемфолдерпасдисплай</span><span class="sxs-lookup"><span data-stu-id="aecd8-103">System.ItemFolderPathDisplay</span></span>

<span data-ttu-id="aecd8-104">Понятный пользователю отображаемый путь к родительской папке элемента.</span><span class="sxs-lookup"><span data-stu-id="aecd8-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="aecd8-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aecd8-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="aecd8-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aecd8-106">Remarks</span></span>

<span data-ttu-id="aecd8-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="aecd8-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="aecd8-108">Если [System. итемпасдисплай](./props-system-itempathdisplay.md) является VT \_ пустым, это свойство также должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="aecd8-108">If [System.ItemPathDisplay](./props-system-itempathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="aecd8-109">В противном случае он должен быть получен соответствующим образом источником данных из System. Итемпасдисплай.</span><span class="sxs-lookup"><span data-stu-id="aecd8-109">Otherwise, it should be derived appropriately by the data source from System.ItemPathDisplay.</span></span>

<span data-ttu-id="aecd8-110">Примеры значений</span><span class="sxs-lookup"><span data-stu-id="aecd8-110">Example values:</span></span>



| <span data-ttu-id="aecd8-111">Путь</span><span class="sxs-lookup"><span data-stu-id="aecd8-111">Path</span></span>                                   | <span data-ttu-id="aecd8-112">итемфолдерпасдисплай</span><span class="sxs-lookup"><span data-stu-id="aecd8-112">ItemFolderPathDisplay</span></span>    |
|----------------------------------------|--------------------------|
| <span data-ttu-id="aecd8-113">c: \\ файлы \\ Personal \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="aecd8-113">c:\\files\\personal\\hello.txt</span></span>         | <span data-ttu-id="aecd8-114">c: \\ файлы \\ личные</span><span class="sxs-lookup"><span data-stu-id="aecd8-114">c:\\files\\personal</span></span>      |
| <span data-ttu-id="aecd8-115">\\\\\\Общая папка сервера \\ MyDir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="aecd8-115">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="aecd8-116">\\\\\\Общая папка сервера \\ MyDir</span><span class="sxs-lookup"><span data-stu-id="aecd8-116">\\\\server\\share\\mydir</span></span> |
| <span data-ttu-id="aecd8-117">\\\\\\Общая папка сервера \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="aecd8-117">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="aecd8-118">\\\\\\Общая папка сервера</span><span class="sxs-lookup"><span data-stu-id="aecd8-118">\\\\server\\share</span></span>        |
| <span data-ttu-id="aecd8-119">в. \\ еда \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="aecd8-119">c:\\food\\MyFolder</span></span>                     | <span data-ttu-id="aecd8-120">c: \\ еда</span><span class="sxs-lookup"><span data-stu-id="aecd8-120">c:\\food</span></span>                 |
| <span data-ttu-id="aecd8-121">Учетная запись/маилбокс/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="aecd8-121">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="aecd8-122">Учетная запись/маилбокс/входящие</span><span class="sxs-lookup"><span data-stu-id="aecd8-122">/Mailbox Account/Inbox</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="aecd8-123">См. также</span><span class="sxs-lookup"><span data-stu-id="aecd8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aecd8-124">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="aecd8-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="aecd8-125">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="aecd8-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="aecd8-126">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="aecd8-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="aecd8-127">typeInfo</span><span class="sxs-lookup"><span data-stu-id="aecd8-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="aecd8-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="aecd8-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="aecd8-129">stringFormat</span><span class="sxs-lookup"><span data-stu-id="aecd8-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="aecd8-130">булеанформат</span><span class="sxs-lookup"><span data-stu-id="aecd8-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="aecd8-131">numberFormat</span><span class="sxs-lookup"><span data-stu-id="aecd8-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="aecd8-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="aecd8-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="aecd8-133">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="aecd8-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="aecd8-134">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="aecd8-134">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="aecd8-135">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="aecd8-135">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="aecd8-136">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="aecd8-136">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="aecd8-137">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="aecd8-137">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
