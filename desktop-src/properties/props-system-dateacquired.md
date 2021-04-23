---
description: Дата приобретения файла или носителя.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. Датеаккуиред
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a85f36df252202c319e90460807e16fefa3d559a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272351"
---
# <a name="systemdateacquired"></a><span data-ttu-id="28fde-103">System. Датеаккуиред</span><span class="sxs-lookup"><span data-stu-id="28fde-103">System.DateAcquired</span></span>

<span data-ttu-id="28fde-104">Дата приобретения файла или носителя.</span><span class="sxs-lookup"><span data-stu-id="28fde-104">The acquisition date of the file or media.</span></span> <span data-ttu-id="28fde-105">Это свойство связано с определенным пользователем или группой пользователей.</span><span class="sxs-lookup"><span data-stu-id="28fde-105">This property is related to a particular user or group of users.</span></span> <span data-ttu-id="28fde-106">Например, эти данные используются в качестве основной оси сортировки для виртуальной папки **Новая музыка**, что позволяет пользователям просматривать последние дополнения к их коллекции.</span><span class="sxs-lookup"><span data-stu-id="28fde-106">For example, this data is used as the main sorting axis for the virtual folder **New Music**, which enables people to browse the latest additions to their collection.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="28fde-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="28fde-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a><span data-ttu-id="28fde-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28fde-108">Windows Vista</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a><span data-ttu-id="28fde-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28fde-109">Remarks</span></span>

<span data-ttu-id="28fde-110">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="28fde-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="28fde-111">[Датеаккуиред]() хранится в виде значения в основном потоке файла, но он может не всегда присутствовать.</span><span class="sxs-lookup"><span data-stu-id="28fde-111">[DateAcquired]() is stored as a value in the main stream of the file, but it may not always be present.</span></span> <span data-ttu-id="28fde-112">В этих случаях Дата приобретения может быть приблизительна на основе других известных дат содержимого.</span><span class="sxs-lookup"><span data-stu-id="28fde-112">In those instances, the acquisition date can be approximated based on other known dates for the content.</span></span> <span data-ttu-id="28fde-113">Обработчик метаданных должен использовать набор правил для определения даты, которую необходимо вернуть.</span><span class="sxs-lookup"><span data-stu-id="28fde-113">The metadata handler should use a set of rules to determine the date to return.</span></span> <span data-ttu-id="28fde-114">В следующем примере демонстрируется использование музыкальных файлов.</span><span class="sxs-lookup"><span data-stu-id="28fde-114">The following example demonstrates this for music files.</span></span>

-   <span data-ttu-id="28fde-115">Для приобретенной музыки следует использовать время создания файла, если приобретенная Дата не указана.</span><span class="sxs-lookup"><span data-stu-id="28fde-115">For purchased music, the file's creation time should be used if no acquired date is present.</span></span> <span data-ttu-id="28fde-116">Однако поставщик загрузки должен задать свойство [датеаккуиред]() в файле.</span><span class="sxs-lookup"><span data-stu-id="28fde-116">However, the download provider should set the [DateAcquired]() property in the file.</span></span>
-   <span data-ttu-id="28fde-117">Чтобы музыкальные файлы были скопированы пользователем или группой (копирование музыки или видео с компакт-диска или DVD-диска на жесткий диск), Дата приобретения должна быть датой выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="28fde-117">For music files that the user or group "ripped" (copying music or video from a CD or DVD to a hard disk), the acquisition date should be the date that action took place.</span></span> <span data-ttu-id="28fde-118">Например, атрибут [WM/енкодингтиме](../wmp/wm-encodingtime-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="28fde-118">For instance, the [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) attribute.</span></span>
-   <span data-ttu-id="28fde-119">Для музыкальных файлов, скопированных из другого расположения, в качестве даты приобретения следует использовать время создания файла.</span><span class="sxs-lookup"><span data-stu-id="28fde-119">For music copied from another location, the file's creation time should be used as the acquisition date.</span></span>

<span data-ttu-id="28fde-120">Примерами [System. датеаккуиред]() являются Дата и время получения изображений с камеры или приобретения музыки через Интернет.</span><span class="sxs-lookup"><span data-stu-id="28fde-120">Examples of [System.DateAcquired]() are the date and time when pictures are acquired from a camera or when music is purchased online.</span></span> <span data-ttu-id="28fde-121">Это не то же самое, что [System. датеимпортед](./props-system-dateimported.md).</span><span class="sxs-lookup"><span data-stu-id="28fde-121">This is not the same as [System.DateImported](./props-system-dateimported.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28fde-122">См. также</span><span class="sxs-lookup"><span data-stu-id="28fde-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28fde-123">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="28fde-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="28fde-124">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="28fde-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="28fde-125">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="28fde-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="28fde-126">typeInfo</span><span class="sxs-lookup"><span data-stu-id="28fde-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="28fde-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="28fde-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="28fde-128">stringFormat</span><span class="sxs-lookup"><span data-stu-id="28fde-128">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="28fde-129">булеанформат</span><span class="sxs-lookup"><span data-stu-id="28fde-129">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="28fde-130">numberFormat</span><span class="sxs-lookup"><span data-stu-id="28fde-130">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="28fde-131">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="28fde-131">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="28fde-132">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="28fde-132">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="28fde-133">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="28fde-133">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="28fde-134">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="28fde-134">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="28fde-135">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="28fde-135">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="28fde-136">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="28fde-136">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
