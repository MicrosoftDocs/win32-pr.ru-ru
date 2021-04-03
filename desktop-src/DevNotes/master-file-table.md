---
description: Основная таблица файлов (MFT) хранит сведения, необходимые для извлечения файлов из раздела NTFS.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Главная таблица файлов (заметки разработчика)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae8656a44b6dadd7d4ff601ddc64623935f5881
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990354"
---
# <a name="master-file-table"></a><span data-ttu-id="8c38f-103">Основная таблица файлов</span><span class="sxs-lookup"><span data-stu-id="8c38f-103">Master File Table</span></span>

<span data-ttu-id="8c38f-104">\[Этот документ применим только к версиям томов NTFS версии 3.\]</span><span class="sxs-lookup"><span data-stu-id="8c38f-104">\[This document applies only to version 3 of NTFS volumes.\]</span></span>

<span data-ttu-id="8c38f-105">Основная таблица файлов (MFT) хранит сведения, необходимые для извлечения файлов из раздела NTFS.</span><span class="sxs-lookup"><span data-stu-id="8c38f-105">The master file table (MFT) stores the information required to retrieve files from an NTFS partition.</span></span>

<span data-ttu-id="8c38f-106">Файл может иметь одну или несколько записей MFT и может содержать один или несколько атрибутов.</span><span class="sxs-lookup"><span data-stu-id="8c38f-106">A file may have one or more MFT records, and can contain one or more attributes.</span></span> <span data-ttu-id="8c38f-107">В файловой системе NTFS ссылка на файл является ссылкой на сегмент MFT основной записи файла.</span><span class="sxs-lookup"><span data-stu-id="8c38f-107">In NTFS, a file reference is the MFT segment reference of the base file record.</span></span> <span data-ttu-id="8c38f-108">Дополнительные сведения см. в [**статье \_ \_ Справочник по сегментам MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8c38f-108">For more information, see [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

<span data-ttu-id="8c38f-109">MFT содержит сегменты записей файлов; первые 16 из них зарезервированы для специальных файлов, например следующих:</span><span class="sxs-lookup"><span data-stu-id="8c38f-109">The MFT contains file record segments; the first 16 of these are reserved for special files, such as the following:</span></span>

-   <span data-ttu-id="8c38f-110">0: MFT ($Mft)</span><span class="sxs-lookup"><span data-stu-id="8c38f-110">0: MFT ($Mft)</span></span>
-   <span data-ttu-id="8c38f-111">5: корневой каталог ( \\ )</span><span class="sxs-lookup"><span data-stu-id="8c38f-111">5: root directory (\\)</span></span>
-   <span data-ttu-id="8c38f-112">6: файл выделения кластера тома ($Bitmap)</span><span class="sxs-lookup"><span data-stu-id="8c38f-112">6: volume cluster allocation file ($Bitmap)</span></span>
-   <span data-ttu-id="8c38f-113">8: Bad — файл кластера ($BadClus)</span><span class="sxs-lookup"><span data-stu-id="8c38f-113">8: bad-cluster file ($BadClus)</span></span>

<span data-ttu-id="8c38f-114">Каждый сегмент записи файла начинается с заголовка сегмента записи файла.</span><span class="sxs-lookup"><span data-stu-id="8c38f-114">Each file record segment starts with a file record segment header.</span></span> <span data-ttu-id="8c38f-115">Дополнительные сведения см. в [**разделе \_ \_ \_ заголовок сегмента записи файла**](file-record-segment-header.md).</span><span class="sxs-lookup"><span data-stu-id="8c38f-115">For more information, see [**FILE\_RECORD\_SEGMENT\_HEADER**](file-record-segment-header.md).</span></span> <span data-ttu-id="8c38f-116">За каждым сегментом записи файла следуют один или несколько атрибутов.</span><span class="sxs-lookup"><span data-stu-id="8c38f-116">Each file record segment is followed by one or more attributes.</span></span> <span data-ttu-id="8c38f-117">Каждый атрибут начинается с заголовка записи атрибута.</span><span class="sxs-lookup"><span data-stu-id="8c38f-117">Each attribute starts with an attribute record header.</span></span> <span data-ttu-id="8c38f-118">Дополнительные сведения см. в [**разделе \_ \_ заголовок записи атрибута**](attribute-record-header.md).</span><span class="sxs-lookup"><span data-stu-id="8c38f-118">For more information, see [**ATTRIBUTE\_RECORD\_HEADER**](attribute-record-header.md).</span></span> <span data-ttu-id="8c38f-119">Запись атрибута включает тип атрибута (например, $DATA или $BITMAP), необязательное имя и значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="8c38f-119">The attribute record includes the attribute type (such as $DATA or $BITMAP), an optional name, and the attribute value.</span></span> <span data-ttu-id="8c38f-120">Пользовательский поток данных — это атрибут, как и все потоки.</span><span class="sxs-lookup"><span data-stu-id="8c38f-120">The user data stream is an attribute, as are all streams.</span></span> <span data-ttu-id="8c38f-121">Список атрибутов завершается с параметром 0xFFFFFFFF ($END).</span><span class="sxs-lookup"><span data-stu-id="8c38f-121">The attribute list is terminated with 0xFFFFFFFF ($END).</span></span>

<span data-ttu-id="8c38f-122">Ниже приведены некоторые примеры атрибутов.</span><span class="sxs-lookup"><span data-stu-id="8c38f-122">The following are some example attributes.</span></span>

-   <span data-ttu-id="8c38f-123">Файл $Mft содержит неименованный $DATA атрибут, который представляет собой последовательность сегментов записи MFT в порядке.</span><span class="sxs-lookup"><span data-stu-id="8c38f-123">The $Mft file contains an unnamed $DATA attribute that is the sequence of MFT record segments, in order.</span></span>
-   <span data-ttu-id="8c38f-124">Файл $Mft содержит неименованный атрибут $BITMAP, который указывает, какие записи MFT используются.</span><span class="sxs-lookup"><span data-stu-id="8c38f-124">The $Mft file contains an unnamed $BITMAP attribute that indicates which MFT records are in use.</span></span>
-   <span data-ttu-id="8c38f-125">Файл $Bitmap содержит неименованный $DATA атрибут, указывающий, какие кластеры используются.</span><span class="sxs-lookup"><span data-stu-id="8c38f-125">The $Bitmap file contains an unnamed $DATA attribute that indicates which clusters are in use.</span></span>
-   <span data-ttu-id="8c38f-126">Файл $BadClus содержит атрибут $DATA с именем $BAD, который содержит запись, соответствующую каждому поврежденному кластеру.</span><span class="sxs-lookup"><span data-stu-id="8c38f-126">The $BadClus file contains a $DATA attribute named $BAD that contains an entry that corresponds to each bad cluster.</span></span>

<span data-ttu-id="8c38f-127">Если больше нет места для хранения атрибутов в сегменте записи файла, то дополнительные сегменты записи файла выделяются и вставляются в первый (или базовый) сегмент записи файла в атрибуте, который называется списком атрибутов.</span><span class="sxs-lookup"><span data-stu-id="8c38f-127">When there is no more space for storing attributes in the file record segment, additional file record segments are allocated and inserted in the first (or base) file record segment in an attribute called the attribute list.</span></span> <span data-ttu-id="8c38f-128">Список атрибутов указывает, где можно найти каждый атрибут, связанный с файлом.</span><span class="sxs-lookup"><span data-stu-id="8c38f-128">The attribute list indicates where each attribute associated with the file can be found.</span></span> <span data-ttu-id="8c38f-129">Сюда входят все атрибуты в записи базового файла, за исключением самого списка атрибутов.</span><span class="sxs-lookup"><span data-stu-id="8c38f-129">This includes all attributes in the base file record, except for the attribute list itself.</span></span> <span data-ttu-id="8c38f-130">Дополнительные сведения см. в [**разделе \_ \_ элемент списка атрибутов**](attribute-list-entry.md).</span><span class="sxs-lookup"><span data-stu-id="8c38f-130">For more information, see [**ATTRIBUTE\_LIST\_ENTRY**](attribute-list-entry.md).</span></span>

<span data-ttu-id="8c38f-131">К структурам MFT относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="8c38f-131">Structures related to the MFT include the following:</span></span>

-   [<span data-ttu-id="8c38f-132">**\_запись списка \_ атрибутов**</span><span class="sxs-lookup"><span data-stu-id="8c38f-132">**ATTRIBUTE\_LIST\_ENTRY**</span></span>](attribute-list-entry.md)
-   [<span data-ttu-id="8c38f-133">**\_заголовок записи \_ атрибута**</span><span class="sxs-lookup"><span data-stu-id="8c38f-133">**ATTRIBUTE\_RECORD\_HEADER**</span></span>](attribute-record-header.md)
-   [<span data-ttu-id="8c38f-134">**\_имя файла**</span><span class="sxs-lookup"><span data-stu-id="8c38f-134">**FILE\_NAME**</span></span>](file-name.md)
-   [<span data-ttu-id="8c38f-135">**\_ \_ заголовок сегмента записи \_ файла**</span><span class="sxs-lookup"><span data-stu-id="8c38f-135">**FILE\_RECORD\_SEGMENT\_HEADER**</span></span>](file-record-segment-header.md)
-   [<span data-ttu-id="8c38f-136">**\_ \_ ссылка на сегмент MFT**</span><span class="sxs-lookup"><span data-stu-id="8c38f-136">**MFT\_SEGMENT\_REFERENCE**</span></span>](mft-segment-reference.md)
-   [<span data-ttu-id="8c38f-137">**заголовок с несколькими \_ секторами \_**</span><span class="sxs-lookup"><span data-stu-id="8c38f-137">**MULTI\_SECTOR\_HEADER**</span></span>](multi-sector-header.md)
-   [<span data-ttu-id="8c38f-138">**СТАНДАРТНЫЕ \_ сведения**</span><span class="sxs-lookup"><span data-stu-id="8c38f-138">**STANDARD\_INFORMATION**</span></span>](standard-information.md)

## <a name="related-topics"></a><span data-ttu-id="8c38f-139">См. также</span><span class="sxs-lookup"><span data-stu-id="8c38f-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8c38f-140">[Технический справочник по NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8c38f-140">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

 
