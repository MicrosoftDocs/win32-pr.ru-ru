---
description: Уникальный идентификатор файла, также известный как номер ссылки на файл.
ms.assetid: 65189671-1b55-4933-9dee-a120b38caa98
title: System. Филефрн
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aa536e0cdda3f42fd9e03315156716ef499c5f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656627"
---
# <a name="systemfilefrn"></a><span data-ttu-id="29343-103">System. Филефрн</span><span class="sxs-lookup"><span data-stu-id="29343-103">System.FileFRN</span></span>

<span data-ttu-id="29343-104">Уникальный идентификатор файла, также известный как номер ссылки на файл.</span><span class="sxs-lookup"><span data-stu-id="29343-104">The unique file ID, also known as the File Reference Number.</span></span> <span data-ttu-id="29343-105">Для данного файла это то же значение, что **и член** [**ID файла с \_ идентификатором « \_ \_ dir \_ info**](/windows/win32/api/winbase/ns-winbase-file_id_both_dir_info) », полученным при вызове [**жетфилеинформатионбихандликс**](/windows/win32/api/winbase/nf-winbase-getfileinformationbyhandleex).</span><span class="sxs-lookup"><span data-stu-id="29343-105">For a given file, this is the same value as the **FileId** member of the [**FILE\_ID\_BOTH\_DIR\_INFO**](/windows/win32/api/winbase/ns-winbase-file_id_both_dir_info) structure, which is obtained by a call to [**GetFileInformationByHandleEx**](/windows/win32/api/winbase/nf-winbase-getfileinformationbyhandleex).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="29343-106">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29343-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.FileFRN
   shellPKey = PKEY_FileFRN
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 21
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt64
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="29343-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29343-107">Remarks</span></span>

<span data-ttu-id="29343-108">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="29343-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29343-109">См. также</span><span class="sxs-lookup"><span data-stu-id="29343-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29343-110">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="29343-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="29343-111">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="29343-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="29343-112">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="29343-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="29343-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="29343-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="29343-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="29343-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="29343-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="29343-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="29343-116">булеанформат</span><span class="sxs-lookup"><span data-stu-id="29343-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="29343-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="29343-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="29343-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="29343-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="29343-119">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="29343-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="29343-120">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="29343-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="29343-121">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="29343-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="29343-122">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="29343-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="29343-123">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="29343-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
