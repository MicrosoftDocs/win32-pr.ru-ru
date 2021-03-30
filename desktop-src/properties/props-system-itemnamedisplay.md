---
description: Отображаемое имя в &\# 0034; наиболее полное&\# 0034; Form.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810984"
---
# <a name="systemitemnamedisplay"></a><span data-ttu-id="37d0f-103">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="37d0f-103">System.ItemNameDisplay</span></span>

<span data-ttu-id="37d0f-104">Отображаемое имя в "наиболее полной" форме.</span><span class="sxs-lookup"><span data-stu-id="37d0f-104">The display name in "most complete" form.</span></span> <span data-ttu-id="37d0f-105">Это уникальное представление имени элемента, наиболее подходящее для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="37d0f-105">It is the unique representation of the item name most appropriate for end users.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="37d0f-106">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37d0f-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="37d0f-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37d0f-107">Remarks</span></span>

<span data-ttu-id="37d0f-108">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="37d0f-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="37d0f-109">Это значение равно конкатентатион для [System. итемнамепрефикс](./props-system-itemnameprefix.md) и [System. ItemName](./props-system-itemname.md).</span><span class="sxs-lookup"><span data-stu-id="37d0f-109">This value is the concatentation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span>

<span data-ttu-id="37d0f-110">Если элемент является файлом, это свойство содержит отображаемое имя, как показано в проводнике.</span><span class="sxs-lookup"><span data-stu-id="37d0f-110">If the item is a file, this property includes the display name as shown in File Explorer.</span></span> <span data-ttu-id="37d0f-111">Существуют допустимые случаи, когда указано свойство [System. имя_файла](./props-system-filename.md) , но значение этого свойства совершенно другое.</span><span class="sxs-lookup"><span data-stu-id="37d0f-111">There are acceptable cases when [System.FileName](./props-system-filename.md) is given but the value of this property is completely different.</span></span> <span data-ttu-id="37d0f-112">Хорошим примером являются сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="37d0f-112">E-mail messages are a good example.</span></span> <span data-ttu-id="37d0f-113">Если элемент является сообщением электронной почты, имя элемента обычно является темой.</span><span class="sxs-lookup"><span data-stu-id="37d0f-113">If the item is an e-mail message, the item name is normally the subject.</span></span> <span data-ttu-id="37d0f-114">В этом случае значение должно быть объединением [System. итемнамепрефикс](./props-system-itemnameprefix.md) и [System. ItemName](./props-system-itemname.md).</span><span class="sxs-lookup"><span data-stu-id="37d0f-114">In that case, the value must be the concatenation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span> <span data-ttu-id="37d0f-115">Поскольку значение System. Итемнамепрефикс исключает все конечные пробелы, при создании [System. итемнамедисплай]()сцепление должно включать пробел.</span><span class="sxs-lookup"><span data-stu-id="37d0f-115">Since the value of System.ItemNamePrefix excludes any trailing spaces, the concatenation must include a space when generating [System.ItemNameDisplay]().</span></span> <span data-ttu-id="37d0f-116">Обратите внимание, что это свойство не обязательно должно быть уникальным, но оно предназначено для продвижения наиболее вероятного кандидата, который может быть уникальным и имеет смысл для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="37d0f-116">Note that this property is not guaranteed to be unique, but is designed to promote the most likely candidate that can be unique and also makes sense to end users.</span></span>

<span data-ttu-id="37d0f-117">Например, для документов можно использовать [System. Title](./props-system-title.md) в качестве [System. итемнамедисплай](), но на практике заголовок документов может оказаться неполезным или уникальным для работы в качестве единственного System. итемнамедисплай.</span><span class="sxs-lookup"><span data-stu-id="37d0f-117">For example, for documents, the [System.Title](./props-system-title.md) could be used as the [System.ItemNameDisplay](), but in practice the title of the documents may not be useful or unique enough to function as the sole System.ItemNameDisplay.</span></span> <span data-ttu-id="37d0f-118">Вместо этого лучше предоставлять [System. filename](./props-system-filename.md) как значение System. итемнамедисплай.</span><span class="sxs-lookup"><span data-stu-id="37d0f-118">Instead, providing [System.FileName](./props-system-filename.md) as the value of System.ItemNameDisplay is a better choice.</span></span> <span data-ttu-id="37d0f-119">В компоненте почта Windows электронная почта хранится в файловой системе в виде EML-файлов.</span><span class="sxs-lookup"><span data-stu-id="37d0f-119">In Windows Mail, e-mail is stored in the file system as .eml files.</span></span> <span data-ttu-id="37d0f-120">Значения System. FileName для этих файлов не являются понятными, так как они являются идентификаторами GUID.</span><span class="sxs-lookup"><span data-stu-id="37d0f-120">The System.FileName values for those files are not human-friendly as they are GUIDs.</span></span> <span data-ttu-id="37d0f-121">В этом примере повышается смысл повышения уровня [System. subject](./props-system-subject.md) как System. итемнамедисплай.</span><span class="sxs-lookup"><span data-stu-id="37d0f-121">In this example, promoting [System.Subject](./props-system-subject.md) as System.ItemNameDisplay makes more sense.</span></span>

<span data-ttu-id="37d0f-122">**Примечания по совместимости:**</span><span class="sxs-lookup"><span data-stu-id="37d0f-122">**Compatibility notes:**</span></span>

-   <span data-ttu-id="37d0f-123">Реализации папок оболочки в Windows Vista: используйте PKEY \_ итемнамедисплай для столбца Name, если нужно, чтобы Проводник Windows вызывал [**ишеллфолдер:: жетдисплайнамеоф**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(шгдн \_ нормаль) для получения значения имени.</span><span class="sxs-lookup"><span data-stu-id="37d0f-123">Shell folder implementations on Windows Vista: use PKEY\_ItemNameDisplay for the name column when you want Windows Explorer to call [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN\_NORMAL) to get the value of the name.</span></span> <span data-ttu-id="37d0f-124">Используйте другой PKEY, например PKEY \_ ItemName, если нужно, чтобы Проводник Windows вызывал либо хранилище свойств папки, либо [**IShellFolder2:: жетдетаилсекс**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) , чтобы получить значение имени.</span><span class="sxs-lookup"><span data-stu-id="37d0f-124">Use another PKEY, such as PKEY\_ItemName, when you want Windows Explorer to call either the folder's property store or [**IShellFolder2::GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) to get the value of the name.</span></span>
-   <span data-ttu-id="37d0f-125">Реализации папок оболочки в Windows XP: первый столбец должен быть столбцом Name, а Проводник Windows вызывает [**ишеллфолдер:: жетдисплайнамеоф**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) , чтобы получить значение имени.</span><span class="sxs-lookup"><span data-stu-id="37d0f-125">Shell folder implementations on Windows XP: the first column must be the name column, and Windows Explorer calls [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to get the value of the name.</span></span> <span data-ttu-id="37d0f-126">Значение PKEY/СЦИД не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="37d0f-126">The PKEY/SCID does not matter.</span></span>



| <span data-ttu-id="37d0f-127">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="37d0f-127">Item type</span></span>     | <span data-ttu-id="37d0f-128">Пример</span><span class="sxs-lookup"><span data-stu-id="37d0f-128">Example</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="37d0f-129">Файл</span><span class="sxs-lookup"><span data-stu-id="37d0f-129">File</span></span>          | <span data-ttu-id="37d0f-130">hello.txt</span><span class="sxs-lookup"><span data-stu-id="37d0f-130">hello.txt</span></span>                 |
| <span data-ttu-id="37d0f-131">Сообщение</span><span class="sxs-lookup"><span data-stu-id="37d0f-131">Message</span></span>       | <span data-ttu-id="37d0f-132">Re: где находится собрание?</span><span class="sxs-lookup"><span data-stu-id="37d0f-132">Re: Where is the meeting?</span></span> |
| <span data-ttu-id="37d0f-133">Папка устройства</span><span class="sxs-lookup"><span data-stu-id="37d0f-133">Device folder</span></span> | <span data-ttu-id="37d0f-134">песня. WMA</span><span class="sxs-lookup"><span data-stu-id="37d0f-134">song.wma</span></span>                  |
| <span data-ttu-id="37d0f-135">Папка</span><span class="sxs-lookup"><span data-stu-id="37d0f-135">Folder</span></span>        | <span data-ttu-id="37d0f-136">Документы</span><span class="sxs-lookup"><span data-stu-id="37d0f-136">Documents</span></span>                 |



 

## <a name="related-topics"></a><span data-ttu-id="37d0f-137">См. также</span><span class="sxs-lookup"><span data-stu-id="37d0f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37d0f-138">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="37d0f-138">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="37d0f-139">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="37d0f-139">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="37d0f-140">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="37d0f-140">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="37d0f-141">typeInfo</span><span class="sxs-lookup"><span data-stu-id="37d0f-141">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="37d0f-142">displayInfo</span><span class="sxs-lookup"><span data-stu-id="37d0f-142">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="37d0f-143">stringFormat</span><span class="sxs-lookup"><span data-stu-id="37d0f-143">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="37d0f-144">булеанформат</span><span class="sxs-lookup"><span data-stu-id="37d0f-144">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="37d0f-145">numberFormat</span><span class="sxs-lookup"><span data-stu-id="37d0f-145">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="37d0f-146">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="37d0f-146">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="37d0f-147">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="37d0f-147">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="37d0f-148">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="37d0f-148">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="37d0f-149">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="37d0f-149">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="37d0f-150">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="37d0f-150">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="37d0f-151">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="37d0f-151">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
