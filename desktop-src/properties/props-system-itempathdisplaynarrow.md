---
description: Прочитайте о свойстве System. Итемпасдисплайнарров, которое представляет понятный пользователю отображаемый путь к элементу.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. Итемпасдисплайнарров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84455a8b69ebf42cb91c191d1c275b70eeeb5ac
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403897"
---
# <a name="systemitempathdisplaynarrow"></a><span data-ttu-id="77e85-103">System. Итемпасдисплайнарров</span><span class="sxs-lookup"><span data-stu-id="77e85-103">System.ItemPathDisplayNarrow</span></span>

<span data-ttu-id="77e85-104">Понятный пользователю отображаемый путь к элементу.</span><span class="sxs-lookup"><span data-stu-id="77e85-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="77e85-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77e85-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="77e85-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="77e85-106">Remarks</span></span>

<span data-ttu-id="77e85-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="77e85-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="77e85-108">Чтобы оптимизировать для столбца с узким просмотром, формат строки должен быть адаптирован, чтобы имя было первым.</span><span class="sxs-lookup"><span data-stu-id="77e85-108">To optimize for a narrow viewing column, the format of the string should be tailored so that the name comes first.</span></span>

<span data-ttu-id="77e85-109">Если элемент является файлом, значение свойства исключает расширение файла, но включает локализованные имена, если они присутствуют.</span><span class="sxs-lookup"><span data-stu-id="77e85-109">If the item is a file, the property value excludes the file extension, but includes localized names if they are present.</span></span> <span data-ttu-id="77e85-110">Если элемент является сообщением, то значение включает параметр [System. итемнамепрефикс](./props-system-itemnameprefix.md).</span><span class="sxs-lookup"><span data-stu-id="77e85-110">If the item is a message, the value includes the [System.ItemNamePrefix](./props-system-itemnameprefix.md).</span></span> <span data-ttu-id="77e85-111">Для синтаксического анализа пути к элементу используйте [System. итемурл](./props-system-itemurl.md) или [System. парсингпас](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="77e85-111">To parse an item path, use [System.ItemUrl](./props-system-itemurl.md) or [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="77e85-112">Примеры значений</span><span class="sxs-lookup"><span data-stu-id="77e85-112">Example values:</span></span>



| <span data-ttu-id="77e85-113">Путь</span><span class="sxs-lookup"><span data-stu-id="77e85-113">Path</span></span>                                   | <span data-ttu-id="77e85-114">итемпасдисплайнаме</span><span class="sxs-lookup"><span data-stu-id="77e85-114">ItemPathDisplayName</span></span>                 |
|----------------------------------------|-------------------------------------|
| <span data-ttu-id="77e85-115">в. \\ \\ линейчатая диаграмма MyDir \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="77e85-115">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="77e85-116">Привет (c: \\ MyDir \\ Bar)</span><span class="sxs-lookup"><span data-stu-id="77e85-116">hello (c:\\mydir\\bar)</span></span>              |
| <span data-ttu-id="77e85-117">\\\\\\Общая папка сервера \\ MyDir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="77e85-117">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="77e85-118">гудневс ( \\ \\ Серверный \\ общий ресурс \\ MyDir)</span><span class="sxs-lookup"><span data-stu-id="77e85-118">goodnews (\\\\server\\share\\mydir)</span></span> |
| <span data-ttu-id="77e85-119">\\\\\\Общая \\ папка сервера</span><span class="sxs-lookup"><span data-stu-id="77e85-119">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="77e85-120">папка ( \\ \\ Общая папка сервера \\ )</span><span class="sxs-lookup"><span data-stu-id="77e85-120">folder (\\\\server\\share)</span></span>          |
| <span data-ttu-id="77e85-121">c: \\ MyDir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="77e85-121">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="77e85-122">MyFolder (c: \\ MyDir)</span><span class="sxs-lookup"><span data-stu-id="77e85-122">MyFolder (c:\\mydir)</span></span>                |
| <span data-ttu-id="77e85-123">Учетная запись/маилбокс/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="77e85-123">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="77e85-124">Повтор: Привет!</span><span class="sxs-lookup"><span data-stu-id="77e85-124">Re: Hello!</span></span> <span data-ttu-id="77e85-125">(Учетная запись/маилбокс/входящие)</span><span class="sxs-lookup"><span data-stu-id="77e85-125">(/Mailbox Account/Inbox)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="77e85-126">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="77e85-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77e85-127">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="77e85-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="77e85-128">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="77e85-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="77e85-129">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="77e85-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="77e85-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="77e85-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="77e85-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="77e85-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="77e85-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="77e85-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="77e85-133">булеанформат</span><span class="sxs-lookup"><span data-stu-id="77e85-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="77e85-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="77e85-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="77e85-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="77e85-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="77e85-136">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="77e85-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="77e85-137">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="77e85-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="77e85-138">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="77e85-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="77e85-139">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="77e85-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="77e85-140">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="77e85-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
