---
description: Канонический тип элемента.
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System. ItemType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0159a12e1cc3c6d85e461461cad20334a641fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272340"
---
# <a name="systemitemtype"></a><span data-ttu-id="1fb0e-103">System. ItemType</span><span class="sxs-lookup"><span data-stu-id="1fb0e-103">System.ItemType</span></span>

<span data-ttu-id="1fb0e-104">Канонический тип элемента.</span><span class="sxs-lookup"><span data-stu-id="1fb0e-104">The canonical type of the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="1fb0e-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fb0e-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="1fb0e-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1fb0e-106">Remarks</span></span>

<span data-ttu-id="1fb0e-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="1fb0e-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="1fb0e-108">Значение System. ItemType предназначено для программного синтаксического анализа и может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="1fb0e-108">The value for System.ItemType is intended to be programmatically parsed, and can be either:</span></span>

-   <span data-ttu-id="1fb0e-109">Расширение файла, которое указывает на значение ProgID ( \_ корень классов hKey \_ \\ <ProgID> ), содержащее отображаемое имя для типа.</span><span class="sxs-lookup"><span data-stu-id="1fb0e-109">A file extension that points to a ProgID value (HKEY\_CLASSES\_ROOT\\<ProgID>) holding the display name for the type.</span></span>
-   <span data-ttu-id="1fb0e-110">Значение ProgID (HKEY \_ Classes \_ ррут \\ <ProgID> ), содержащее отображаемое имя для типа.</span><span class="sxs-lookup"><span data-stu-id="1fb0e-110">A ProgID value (HKEY\_CLASSES\_RROOT\\<ProgID>), containing the display name for the type.</span></span>

<span data-ttu-id="1fb0e-111">Элемент Фриендлитипенаме ProgID должен быть локализованной версией имени приложения ( @winword.dll -42), а значение по умолчанию для ключа ProgID — нелокализованным именем (Word.Docумент. 12).</span><span class="sxs-lookup"><span data-stu-id="1fb0e-111">The FriendlyTypeName element of a ProgID should be a localized version of the application name (@winword.dll,-42), while the default value of the ProgID key is a non-localized name (Word.Document.12).</span></span>

<span data-ttu-id="1fb0e-112">Если канонического типа нет, это значение является VT \_ пустым.</span><span class="sxs-lookup"><span data-stu-id="1fb0e-112">If there is no canonical type, the value is VT\_EMPTY.</span></span> <span data-ttu-id="1fb0e-113">Если элемент является файлом ([System. filename](./props-system-filename.md) не является VT \_ ), то значение совпадает с [System. fileExtension](./props-system-fileextension.md).</span><span class="sxs-lookup"><span data-stu-id="1fb0e-113">If the item is a file ([System.FileName](./props-system-filename.md) is not VT\_EMPTY), the value is the same as [System.FileExtension](./props-system-fileextension.md).</span></span> <span data-ttu-id="1fb0e-114">Используйте [System. итемтипетекст](./props-system-itemtypetext.md) , если нужно отобразить тип для конечных пользователей в представлении.</span><span class="sxs-lookup"><span data-stu-id="1fb0e-114">Use [System.ItemTypeText](./props-system-itemtypetext.md) when you want to display the type to end users in a view.</span></span>

> [!Note]  
> <span data-ttu-id="1fb0e-115">Если элемент является файлом, передача значения [System. ItemType]() в [**псформатфордисплай**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) приведет к тому же значению, что и [System. итемтипетекст](./props-system-itemtypetext.md).</span><span class="sxs-lookup"><span data-stu-id="1fb0e-115">If the item is a file, passing the [System.ItemType]() value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) results in the same value as [System.ItemTypeText](./props-system-itemtypetext.md).</span></span>

 

<span data-ttu-id="1fb0e-116">Примеры значений</span><span class="sxs-lookup"><span data-stu-id="1fb0e-116">Example values:</span></span>



| <span data-ttu-id="1fb0e-117">Путь</span><span class="sxs-lookup"><span data-stu-id="1fb0e-117">Path</span></span>                                   | <span data-ttu-id="1fb0e-118">ItemType</span><span class="sxs-lookup"><span data-stu-id="1fb0e-118">ItemType</span></span>         |
|----------------------------------------|------------------|
| <span data-ttu-id="1fb0e-119">в. \\ \\ линейчатая диаграмма MyDir \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="1fb0e-119">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="1fb0e-120">.txt</span><span class="sxs-lookup"><span data-stu-id="1fb0e-120">.txt</span></span>             |
| <span data-ttu-id="1fb0e-121">\\\\\\Общая папка сервера \\ MyDir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="1fb0e-121">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="1fb0e-122">.doc</span><span class="sxs-lookup"><span data-stu-id="1fb0e-122">.doc</span></span>             |
| <span data-ttu-id="1fb0e-123">\\\\\\Общая \\ папка сервера</span><span class="sxs-lookup"><span data-stu-id="1fb0e-123">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="1fb0e-124">Каталог</span><span class="sxs-lookup"><span data-stu-id="1fb0e-124">Directory</span></span>        |
| <span data-ttu-id="1fb0e-125">c: \\ MyDir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="1fb0e-125">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="1fb0e-126">Каталог</span><span class="sxs-lookup"><span data-stu-id="1fb0e-126">Directory</span></span>        |
| <span data-ttu-id="1fb0e-127">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="1fb0e-127">\[desktop\]</span></span>                            | <span data-ttu-id="1fb0e-128">Папка</span><span class="sxs-lookup"><span data-stu-id="1fb0e-128">Folder</span></span>           |
| <span data-ttu-id="1fb0e-129">Учетная запись/маилбокс/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="1fb0e-129">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="1fb0e-130">MAPI/IPM. Сообщение</span><span class="sxs-lookup"><span data-stu-id="1fb0e-130">MAPI/IPM.Message</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1fb0e-131">См. также</span><span class="sxs-lookup"><span data-stu-id="1fb0e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fb0e-132">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="1fb0e-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-133">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="1fb0e-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-134">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="1fb0e-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-135">typeInfo</span><span class="sxs-lookup"><span data-stu-id="1fb0e-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-136">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1fb0e-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-137">stringFormat</span><span class="sxs-lookup"><span data-stu-id="1fb0e-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-138">булеанформат</span><span class="sxs-lookup"><span data-stu-id="1fb0e-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-139">numberFormat</span><span class="sxs-lookup"><span data-stu-id="1fb0e-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1fb0e-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-141">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="1fb0e-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-142">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="1fb0e-142">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-143">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="1fb0e-143">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-144">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="1fb0e-144">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-145">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="1fb0e-145">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="1fb0e-146">Программные идентификаторы</span><span class="sxs-lookup"><span data-stu-id="1fb0e-146">Programmatic Identifiers</span></span>](../shell/fa-progids.md)
</dt> </dl>

 

 
