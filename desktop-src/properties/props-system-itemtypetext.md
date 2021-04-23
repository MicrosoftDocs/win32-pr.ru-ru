---
description: Понятное пользователю имя типа элемента.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. Итемтипетекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699a953392054cb2344c5f3b3d652e64a9a2c1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264258"
---
# <a name="systemitemtypetext"></a><span data-ttu-id="9ba25-103">System. Итемтипетекст</span><span class="sxs-lookup"><span data-stu-id="9ba25-103">System.ItemTypeText</span></span>

<span data-ttu-id="9ba25-104">Понятное пользователю имя типа элемента.</span><span class="sxs-lookup"><span data-stu-id="9ba25-104">The user-friendly type name of the item.</span></span> <span data-ttu-id="9ba25-105">Это значение не предназначено для программного синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="9ba25-105">This value is not intended to be programmatically parsed.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="9ba25-106">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ba25-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="9ba25-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ba25-107">Remarks</span></span>

<span data-ttu-id="9ba25-108">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="9ba25-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="9ba25-109">Если [System. ItemType](./props-system-itemtype.md) является VT \_ пустым, значение этого свойства также является VT \_ пустым.</span><span class="sxs-lookup"><span data-stu-id="9ba25-109">If [System.ItemType](./props-system-itemtype.md) is VT\_EMPTY, the value of this property is also VT\_EMPTY.</span></span> <span data-ttu-id="9ba25-110">Если элемент является файлом, значение этого свойства будет таким же, как если бы значение System. ItemType файла было передано в [**псформатфордисплай**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).</span><span class="sxs-lookup"><span data-stu-id="9ba25-110">If the item is a file, the value of this property is the same as if you passed the file's System.ItemType value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).</span></span>

<span data-ttu-id="9ba25-111">Это свойство не следует путать с [System. Kind](./props-system-kind.md), которое представляет собой высокоуровневое понятное имя типа.</span><span class="sxs-lookup"><span data-stu-id="9ba25-111">This property should not be confused with [System.Kind](./props-system-kind.md), which is a high-level, user-friendly kind name.</span></span> <span data-ttu-id="9ba25-112">Например, для DOC-файла документа используются различные свойства, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="9ba25-112">For example, for a .doc document file, the various properties are as shown here:</span></span>



| <span data-ttu-id="9ba25-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="9ba25-113">Property</span></span>                                               | <span data-ttu-id="9ba25-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9ba25-114">Value</span></span>                   |
|--------------------------------------------------------|-------------------------|
| [<span data-ttu-id="9ba25-115">System. Kind</span><span class="sxs-lookup"><span data-stu-id="9ba25-115">System.Kind</span></span>](./props-system-kind.md)                 | <span data-ttu-id="9ba25-116">Документ</span><span class="sxs-lookup"><span data-stu-id="9ba25-116">Document</span></span>                |
| [<span data-ttu-id="9ba25-117">System. ItemType</span><span class="sxs-lookup"><span data-stu-id="9ba25-117">System.ItemType</span></span>](./props-system-itemtype.md)         | <span data-ttu-id="9ba25-118">.doc</span><span class="sxs-lookup"><span data-stu-id="9ba25-118">.doc</span></span>                    |
| [<span data-ttu-id="9ba25-119">System. Итемтипетекст</span><span class="sxs-lookup"><span data-stu-id="9ba25-119">System.ItemTypeText</span></span>]() | <span data-ttu-id="9ba25-120">Документ Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="9ba25-120">Microsoft Word Document</span></span> |



 

<span data-ttu-id="9ba25-121">Примеры значений</span><span class="sxs-lookup"><span data-stu-id="9ba25-121">Example values:</span></span>



| <span data-ttu-id="9ba25-122">Путь</span><span class="sxs-lookup"><span data-stu-id="9ba25-122">Path</span></span>                                   | <span data-ttu-id="9ba25-123">итемтипетекст</span><span class="sxs-lookup"><span data-stu-id="9ba25-123">ItemTypeText</span></span>            |
|----------------------------------------|-------------------------|
| <span data-ttu-id="9ba25-124">в. \\ \\ линейчатая диаграмма MyDir \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="9ba25-124">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="9ba25-125">Текстовый файл</span><span class="sxs-lookup"><span data-stu-id="9ba25-125">Text File</span></span>               |
| <span data-ttu-id="9ba25-126">\\\\\\Общая папка сервера \\ MyDir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="9ba25-126">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="9ba25-127">Документ Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="9ba25-127">Microsoft Word Document</span></span> |
| <span data-ttu-id="9ba25-128">\\\\\\Общая \\ папка сервера</span><span class="sxs-lookup"><span data-stu-id="9ba25-128">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="9ba25-129">Папка с файлами</span><span class="sxs-lookup"><span data-stu-id="9ba25-129">File Folder</span></span>             |
| <span data-ttu-id="9ba25-130">c: \\ MyDir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="9ba25-130">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="9ba25-131">Папка с файлами</span><span class="sxs-lookup"><span data-stu-id="9ba25-131">File Folder</span></span>             |
| <span data-ttu-id="9ba25-132">Учетная запись/маилбокс/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="9ba25-132">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="9ba25-133">Сообщение электронной почты Outlook</span><span class="sxs-lookup"><span data-stu-id="9ba25-133">Outlook E-Mail Message</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="9ba25-134">См. также</span><span class="sxs-lookup"><span data-stu-id="9ba25-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ba25-135">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="9ba25-135">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="9ba25-136">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="9ba25-136">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="9ba25-137">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="9ba25-137">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="9ba25-138">typeInfo</span><span class="sxs-lookup"><span data-stu-id="9ba25-138">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="9ba25-139">displayInfo</span><span class="sxs-lookup"><span data-stu-id="9ba25-139">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="9ba25-140">stringFormat</span><span class="sxs-lookup"><span data-stu-id="9ba25-140">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="9ba25-141">булеанформат</span><span class="sxs-lookup"><span data-stu-id="9ba25-141">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="9ba25-142">numberFormat</span><span class="sxs-lookup"><span data-stu-id="9ba25-142">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="9ba25-143">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="9ba25-143">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="9ba25-144">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="9ba25-144">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="9ba25-145">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="9ba25-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="9ba25-146">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="9ba25-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="9ba25-147">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="9ba25-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="9ba25-148">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="9ba25-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
