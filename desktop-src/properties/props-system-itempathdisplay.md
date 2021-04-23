---
description: Понятный пользователю отображаемый путь к элементу.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. Итемпасдисплай
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb76a4218e7e7580ec70cb57dd16c635ca024ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156419"
---
# <a name="systemitempathdisplay"></a><span data-ttu-id="2c8b6-103">System. Итемпасдисплай</span><span class="sxs-lookup"><span data-stu-id="2c8b6-103">System.ItemPathDisplay</span></span>

<span data-ttu-id="2c8b6-104">Понятный пользователю отображаемый путь к элементу.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="2c8b6-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c8b6-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="2c8b6-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c8b6-106">Remarks</span></span>

<span data-ttu-id="2c8b6-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="2c8b6-108">Если элемент является файлом или папкой, это свойство включает расширение во всех случаях и локализуется, если локализованное имя доступно.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-108">If the item is a file or folder, this property includes the extension in all cases, and is localized if a localized name is available.</span></span> <span data-ttu-id="2c8b6-109">Для других элементов это понятный для пользователя эквивалент, предполагая, что элемент существует в иерархическом хранилище.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-109">For other items, this is the user-friendly equivalent, assuming that the item exists in hierarchical storage.</span></span>

<span data-ttu-id="2c8b6-110">В отличие от [System. итемурл](./props-system-itemurl.md), это значение свойства не включает схему URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-110">Unlike [System.ItemUrl](./props-system-itemurl.md), this property value does not include the URL scheme.</span></span> <span data-ttu-id="2c8b6-111">Для синтаксического анализа пути к элементу используйте System. Итемурл или [System. парсингпас](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="2c8b6-111">To parse an item path, use System.ItemUrl or [System.ParsingPath](./props-system-parsingpath.md).</span></span> <span data-ttu-id="2c8b6-112">Для ссылки на элементы пространства имен оболочки с помощью интерфейсов API оболочки используйте System. Парсингпас.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-112">To reference Shell namespace items using Shell APIs, use System.ParsingPath.</span></span>

<span data-ttu-id="2c8b6-113">Примеры значений</span><span class="sxs-lookup"><span data-stu-id="2c8b6-113">Example values:</span></span>



| <span data-ttu-id="2c8b6-114">Путь</span><span class="sxs-lookup"><span data-stu-id="2c8b6-114">Path</span></span>                                   | <span data-ttu-id="2c8b6-115">итемпасдисплай</span><span class="sxs-lookup"><span data-stu-id="2c8b6-115">ItemPathDisplay</span></span>                        |
|----------------------------------------|----------------------------------------|
| <span data-ttu-id="2c8b6-116">в. \\ \\ линейчатая диаграмма MyDir \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="2c8b6-116">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="2c8b6-117">в. \\ \\ линейчатая диаграмма MyDir \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="2c8b6-117">c:\\mydir\\bar\\hello.txt</span></span>              |
| <span data-ttu-id="2c8b6-118">\\\\\\Общая папка сервера \\ MyDir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="2c8b6-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="2c8b6-119">\\\\\\Общая папка сервера \\ MyDir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="2c8b6-119">\\\\server\\share\\mydir\\goodnews.doc</span></span> |
| <span data-ttu-id="2c8b6-120">\\\\\\Общая папка сервера \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="2c8b6-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="2c8b6-121">\\\\\\Общая папка сервера \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="2c8b6-121">\\\\server\\share\\numbers.xls</span></span>         |
| <span data-ttu-id="2c8b6-122">c: \\ MyDir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="2c8b6-122">c:\\mydir\\MyFolder</span></span>                    | <span data-ttu-id="2c8b6-123">c: \\ MyDir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="2c8b6-123">c:\\mydir\\MyFolder</span></span>                    |
| <span data-ttu-id="2c8b6-124">Учетная запись/маилбокс/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="2c8b6-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="2c8b6-125">Учетная запись/маилбокс/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="2c8b6-125">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="2c8b6-126">См. также</span><span class="sxs-lookup"><span data-stu-id="2c8b6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c8b6-127">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="2c8b6-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-128">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="2c8b6-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-129">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="2c8b6-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="2c8b6-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2c8b6-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2c8b6-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-133">булеанформат</span><span class="sxs-lookup"><span data-stu-id="2c8b6-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="2c8b6-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2c8b6-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-136">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="2c8b6-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-137">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="2c8b6-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-138">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="2c8b6-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-139">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="2c8b6-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2c8b6-140">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="2c8b6-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
