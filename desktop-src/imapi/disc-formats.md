---
title: Форматы дисков
description: 'IMAPI поддерживает три формата файловой системы: ISO 9660, Жолиет и UDF.'
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9b4d4c5c5b6aa3e0c4c96598486a531c297b61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330088"
---
# <a name="disc-formats"></a><span data-ttu-id="5464d-103">Форматы дисков</span><span class="sxs-lookup"><span data-stu-id="5464d-103">Disc Formats</span></span>

<span data-ttu-id="5464d-104">IMAPI поддерживает три формата файловой системы: [ISO 9660](#iso-9660), [Жолиет](#joliet)и [UDF](#universal-disk-format-udf).</span><span class="sxs-lookup"><span data-stu-id="5464d-104">IMAPI supports three file system formats: [ISO 9660](#iso-9660), [Joliet](#joliet), and [UDF](#universal-disk-format-udf).</span></span>

## <a name="iso-9660"></a><span data-ttu-id="5464d-105">ISO 9660</span><span class="sxs-lookup"><span data-stu-id="5464d-105">ISO 9660</span></span>

<span data-ttu-id="5464d-106">Формат ISO 9660 — это исходная Стандартная файловая система для дисков с данными компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="5464d-106">The ISO 9660 format is the original standard file system for CD data discs.</span></span> <span data-ttu-id="5464d-107">Формат распознается в нескольких операционных системах, включая MSDOS, Mac OS, UNIX и операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="5464d-107">The format is recognized on several operating systems, including MSDOS, the Mac OS, UNIX, and the Windows operating system.</span></span> <span data-ttu-id="5464d-108">Формат ISO 9660 публикуется Международная организация по стандартизации (ISO).</span><span class="sxs-lookup"><span data-stu-id="5464d-108">The ISO 9660 format is published by the International Organization for Standardization (ISO).</span></span>

<span data-ttu-id="5464d-109">Формат начинается в секторе 16 с заголовком тома CD0001; Оставшаяся часть заголовка выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="5464d-109">The format begins at sector 16 with the volume header, CD0001; the remainder of the header follows.</span></span> <span data-ttu-id="5464d-110">Другие производные форматы также начинаются с сектора 16, но используют другую строку для заголовка тома.</span><span class="sxs-lookup"><span data-stu-id="5464d-110">Other derived formats also begin at sector 16, but use another string for the volume header.</span></span> <span data-ttu-id="5464d-111">Например, высокие диски с высоким преобразованием используют в качестве строкового формата CD-ROM0001 и компакт-диска параметр reI0001.</span><span class="sxs-lookup"><span data-stu-id="5464d-111">For example, High Sierra discs use the string CD-ROM0001 and Compact Disc Interactive format uses CD-I0001.</span></span>

<span data-ttu-id="5464d-112">Заголовок указывает на области диска, в котором хранятся имена файлов в формате ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="5464d-112">The header points to areas of the disc that store the file names in ISO 9660 format.</span></span> <span data-ttu-id="5464d-113">Соглашение об именовании файлов и каталогов состоит из 8 символов, точки и еще 3 символов.</span><span class="sxs-lookup"><span data-stu-id="5464d-113">The file and directory naming convention consists of 8 characters, a period, and 3 more characters.</span></span> <span data-ttu-id="5464d-114">Это то же соглашение об именовании, которое используется операционной системой MSDOS.</span><span class="sxs-lookup"><span data-stu-id="5464d-114">This is the same naming convention used by the MSDOS operating system.</span></span>

<span data-ttu-id="5464d-115">Дополнительные заголовки файловой системы для форматов, таких как Жолиет и UDF, могут сосуществовать на диске, не влияя на удобочитаемость формата ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="5464d-115">Additional file system headers, for formats such as Joliet and UDF, can co-exist on a disc without affecting the readability of the ISO 9660 format.</span></span> <span data-ttu-id="5464d-116">После индексов набор файлов данных займет диск. Индексы для каждой файловой системы независимо зависят от файлов данных на диске.</span><span class="sxs-lookup"><span data-stu-id="5464d-116">After the indexes, a set of data files occupy the disc. The indexes for each file system independently reference data files on the disc.</span></span>

<span data-ttu-id="5464d-117">Спецификация ISO 9660 определяет три уровня формата:</span><span class="sxs-lookup"><span data-stu-id="5464d-117">The ISO 9660 specification defines three levels of the format:</span></span>

-   <span data-ttu-id="5464d-118">Уровень 1 определяет имена файлов для использования символьного формата 8,3.</span><span class="sxs-lookup"><span data-stu-id="5464d-118">Level 1 defines file names to use the 8.3 character format.</span></span>
-   <span data-ttu-id="5464d-119">Уровень 2 позволяет использовать более длинные имена файлов, как это было показано на платформах DOS 6. XX, MacIntosh и UNIX.</span><span class="sxs-lookup"><span data-stu-id="5464d-119">Level 2 permits longer file names, as found on DOS 6.xx, MacIntosh, and UNIX platforms.</span></span>
-   <span data-ttu-id="5464d-120">Уровень 3 разрешает чередование данных и звуковых файлов для повышения производительности извлечения (воспроизведения).</span><span class="sxs-lookup"><span data-stu-id="5464d-120">Level 3 allows interleaved data and audio files to improve retrieval (playback) performance.</span></span> <span data-ttu-id="5464d-121">На этом уровне также удаляется ограничение в 2 ГБ файла.</span><span class="sxs-lookup"><span data-stu-id="5464d-121">This level also removes the 2GB file limit.</span></span> <span data-ttu-id="5464d-122">Этот уровень **не** поддерживается API-интерфейсом основного образа.</span><span class="sxs-lookup"><span data-stu-id="5464d-122">This level is **not** supported by the Image Mastering API.</span></span>

<span data-ttu-id="5464d-123">DVD-диски также могут использовать ISO 9660; Однако файловая система UDF — это наиболее распространенная файловая система, используемая с DVD-носителями.</span><span class="sxs-lookup"><span data-stu-id="5464d-123">DVD discs can also use ISO 9660; however, the UDF file system is the most prevalent file system used with DVD media.</span></span>

## <a name="joliet"></a><span data-ttu-id="5464d-124">жолиет</span><span class="sxs-lookup"><span data-stu-id="5464d-124">Joliet</span></span>

<span data-ttu-id="5464d-125">Формат Жолиет является производным от ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="5464d-125">The Joliet format is a derivative of ISO 9660.</span></span> <span data-ttu-id="5464d-126">Этот формат записывает индекс файловой системы Жолиет в образ диска в дополнение к индексу файловой системы ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="5464d-126">This format writes the Joliet file system index to the disc image in addition to the ISO 9660 file system index.</span></span>

<span data-ttu-id="5464d-127">Индекс Жолиет обеспечивает следующие улучшения в индексе файловой системы.</span><span class="sxs-lookup"><span data-stu-id="5464d-127">The Joliet index provides the following improvements to the file system index:</span></span>

-   <span data-ttu-id="5464d-128">Распознает длинные имена файлов длиной до 32 символов.</span><span class="sxs-lookup"><span data-stu-id="5464d-128">Recognizes long file names up to 32 characters.</span></span>
-   <span data-ttu-id="5464d-129">Различия между буквами верхнего и нижнего регистра в именах файлов.</span><span class="sxs-lookup"><span data-stu-id="5464d-129">Distinguishes between upper and lower case letters in the file names.</span></span>
-   <span data-ttu-id="5464d-130">Поддерживает символы Юникода в имени файла.</span><span class="sxs-lookup"><span data-stu-id="5464d-130">Supports Unicode characters in the filename.</span></span>

<span data-ttu-id="5464d-131">Заголовок формата Жолиет начинается в секторе 17 диска.</span><span class="sxs-lookup"><span data-stu-id="5464d-131">The Joliet format header begins at sector 17 of the disc.</span></span>

<span data-ttu-id="5464d-132">Так как формат Жолиет сохраняет файловую систему ISO 9660 на диске, сохраняется совместимость с устройствами, совместимыми с ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="5464d-132">Because the Joliet format preserves the ISO 9660 file system on a disc, compatibility with ISO 9660-compliant devices is retained.</span></span>

## <a name="universal-disk-format-udf"></a><span data-ttu-id="5464d-133">Формат UDF</span><span class="sxs-lookup"><span data-stu-id="5464d-133">Universal Disk Format (UDF)</span></span>

<span data-ttu-id="5464d-134">Универсальный формат диска (UDF) — это новая файловая система, разработанная для оптического носителя с помощью технологии оптического хранилища (ОСТА).</span><span class="sxs-lookup"><span data-stu-id="5464d-134">The Universal Disk Format (UDF) is a newer file system developed for optical media by the Optical Storage Technology Association (OSTA).</span></span> <span data-ttu-id="5464d-135">UDF — это переносимый формат, распознаваемый несколькими операционными системами.</span><span class="sxs-lookup"><span data-stu-id="5464d-135">UDF is a portable format that is recognized by several operating systems.</span></span> <span data-ttu-id="5464d-136">UDF заменяет стандарт ISO 9660 в качестве нового стандарта, особенно с носителями, предназначенными для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5464d-136">UDF is replacing ISO 9660 as the new standard, especially with read/write media.</span></span>

<span data-ttu-id="5464d-137">К функциям UDF относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="5464d-137">Features of UDF include the following:</span></span>

-   <span data-ttu-id="5464d-138">Поддерживает носители размером до 2 ТБ.</span><span class="sxs-lookup"><span data-stu-id="5464d-138">Supports media up to 2TB in size.</span></span>
-   <span data-ttu-id="5464d-139">Поддерживает файлы Flash Media, Iomega-диски и диски CD МРВ.</span><span class="sxs-lookup"><span data-stu-id="5464d-139">Supports flash media, Iomega REV discs, and CD-MRW discs.</span></span>
-   <span data-ttu-id="5464d-140">Хранит файлы размером менее 2 КБ в блоке записи файла.</span><span class="sxs-lookup"><span data-stu-id="5464d-140">Stores files less than 2 KB in length in the File Entry block.</span></span>
-   <span data-ttu-id="5464d-141">Поддерживает файлы размером до 2 ТБ с именами файлов длиной 255 символов.</span><span class="sxs-lookup"><span data-stu-id="5464d-141">Supports files up to 2TB with filenames as long as 255 characters.</span></span>
-   <span data-ttu-id="5464d-142">Поддерживает обширный набор атрибутов файлов, отвечающих различным операционным системам.</span><span class="sxs-lookup"><span data-stu-id="5464d-142">Supports a rich set of file attributes that suit various operating systems.</span></span>
-   <span data-ttu-id="5464d-143">Поддерживает формат моста, в котором все форматы ISO 9660, Жолиет и UDF находятся на одном и том же диске. Он используется в видеороликах, таких как DVD-видео, DVD + VR и DVD-VR.</span><span class="sxs-lookup"><span data-stu-id="5464d-143">Supports a bridge format where ISO 9660, Joliet, and UDF formats all reside on the same disc. This is used in video applications, such as DVD-Video, DVD+VR, and DVD-VR.</span></span>
-   <span data-ttu-id="5464d-144">Поддерживает именованные потоки и файлы в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="5464d-144">Supports named streams and 'Real-Time' files.</span></span>

 

 




