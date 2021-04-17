---
title: Интерфейсы IMAPI
description: В следующих таблицах приведены и кратко описаны интерфейсы, используемые разработчиками C/C++ и связанным объектом скрипта. Добавьте в таблицу имя объекта с параметром \ 0034; IMAPI2. \ 0034; для полного определения имени объекта при создании объекта в скрипте.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac989a9871b761a1f1700ec599cc51affd30b2e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "105681578"
---
# <a name="imapi-interfaces"></a><span data-ttu-id="e375d-105">Интерфейсы IMAPI</span><span class="sxs-lookup"><span data-stu-id="e375d-105">IMAPI Interfaces</span></span>

<span data-ttu-id="e375d-106">В следующих таблицах приведены и кратко описаны интерфейсы, используемые разработчиками C/C++ и связанным объектом скрипта.</span><span class="sxs-lookup"><span data-stu-id="e375d-106">The following tables identify and briefly describe the interfaces used C/C++ developers and the associated scripting object.</span></span> <span data-ttu-id="e375d-107">Добавьте перед именем объекта в таблице "IMAPI2".</span><span class="sxs-lookup"><span data-stu-id="e375d-107">Prefix the object name in the table with "IMAPI2."</span></span> <span data-ttu-id="e375d-108">для полного определения имени объекта при создании объекта в скрипте.</span><span class="sxs-lookup"><span data-stu-id="e375d-108">to fully qualify the object name when creating the object in script.</span></span>

<span data-ttu-id="e375d-109">В следующей таблице перечислены интерфейсы, связанные с устройствами, подсистемой записи и форматами записи и стирания форматирования.</span><span class="sxs-lookup"><span data-stu-id="e375d-109">The following table lists the interfaces associated with devices, the burn engine, and the format writers and eraser.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e375d-110">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="e375d-110">Interface</span></span></td>
<td><span data-ttu-id="e375d-111">Объект</span><span class="sxs-lookup"><span data-stu-id="e375d-111">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-112">Высокоуровневая подсистема записи.</span><span class="sxs-lookup"><span data-stu-id="e375d-112">Low-level burn engine.</span></span>
<ul>
<li><span data-ttu-id="e375d-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span></span></li>
<li><span data-ttu-id="e375d-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span></span></li>
<li><span data-ttu-id="e375d-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-116">MsftWriteEngine2</span><span class="sxs-lookup"><span data-stu-id="e375d-116">MsftWriteEngine2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-117">Основной модуль записи образов.</span><span class="sxs-lookup"><span data-stu-id="e375d-117">Main image writer.</span></span>
<ul>
<li><span data-ttu-id="e375d-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span></span></li>
<li><span data-ttu-id="e375d-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span></span></li>
<li><span data-ttu-id="e375d-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-121">MsftDiscFormat2Data</span><span class="sxs-lookup"><span data-stu-id="e375d-121">MsftDiscFormat2Data</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-122">Ластик для дисков.</span><span class="sxs-lookup"><span data-stu-id="e375d-122">Disc eraser.</span></span>
<ul>
<li><span data-ttu-id="e375d-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span></span></li>
<li><span data-ttu-id="e375d-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-125">MsftDiscFormat2Erase</span><span class="sxs-lookup"><span data-stu-id="e375d-125">MsftDiscFormat2Erase</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-126">Необработанный модуль записи изображений.</span><span class="sxs-lookup"><span data-stu-id="e375d-126">Raw image writer.</span></span>
<ul>
<li><span data-ttu-id="e375d-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span></span></li>
<li><span data-ttu-id="e375d-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span></span></li>
<li><span data-ttu-id="e375d-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-130">MsftDiscFormat2RawCD</span><span class="sxs-lookup"><span data-stu-id="e375d-130">MsftDiscFormat2RawCD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-131">Средство записи образов в один раз.</span><span class="sxs-lookup"><span data-stu-id="e375d-131">Track-At-Once image writer.</span></span>
<ul>
<li><span data-ttu-id="e375d-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span></span></li>
<li><span data-ttu-id="e375d-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span></span></li>
<li><span data-ttu-id="e375d-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-135">MsftDiscFormat2TrackAtOnce</span><span class="sxs-lookup"><span data-stu-id="e375d-135">MsftDiscFormat2TrackAtOnce</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-136">Перечисление дисковых устройств в списке оборудования системы.</span><span class="sxs-lookup"><span data-stu-id="e375d-136">Enumeration of disc devices in the system hardware list.</span></span>
<ul>
<li><span data-ttu-id="e375d-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-138">MsftDiscMaster2</span><span class="sxs-lookup"><span data-stu-id="e375d-138">MsftDiscMaster2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-139">Делегат уведомления для объекта MsftDiscMaster2.</span><span class="sxs-lookup"><span data-stu-id="e375d-139">Notification delegate for the MsftDiscMaster2 object.</span></span>
<ul>
<li><span data-ttu-id="e375d-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-141">DDiscMaster2Events</span><span class="sxs-lookup"><span data-stu-id="e375d-141">DDiscMaster2Events</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-142">Отдельное устройство записи.</span><span class="sxs-lookup"><span data-stu-id="e375d-142">Individual recording device.</span></span>
<ul>
<li><span data-ttu-id="e375d-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span></span></li>
<li><span data-ttu-id="e375d-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-145">MsftDiscRecorder2</span><span class="sxs-lookup"><span data-stu-id="e375d-145">MsftDiscRecorder2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-146">Атрибуты записи устройства, включая тип носителя, скорость записи и тип углового элемента управления скоростью.</span><span class="sxs-lookup"><span data-stu-id="e375d-146">Device writing attributes, including the media type, writing speed, and type of angular velocity control.</span></span>
<ul>
<li><span data-ttu-id="e375d-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>ивритеспиддескриптор</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-148">мсфтвритеспиддескриптор</span><span class="sxs-lookup"><span data-stu-id="e375d-148">MsftWriteSpeedDescriptor</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e375d-149">В следующей таблице перечислены интерфейсы файловой системы.</span><span class="sxs-lookup"><span data-stu-id="e375d-149">The following table lists the file system interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e375d-150">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="e375d-150">Interface</span></span></td>
<td><span data-ttu-id="e375d-151">Объект</span><span class="sxs-lookup"><span data-stu-id="e375d-151">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-152">Поток загрузочного образа и свойства для интеграции загрузочного образа в образ диска.</span><span class="sxs-lookup"><span data-stu-id="e375d-152">Boot image stream and properties for integrating the bootable image in the disc image.</span></span>
<ul>
<li><span data-ttu-id="e375d-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>ибутоптионс</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-154">бутоптионс</span><span class="sxs-lookup"><span data-stu-id="e375d-154">BootOptions</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-155">Образ и свойства файловой системы.</span><span class="sxs-lookup"><span data-stu-id="e375d-155">File system image and properties.</span></span> <span data-ttu-id="e375d-156">Этот объект включает все записи и ссылки на образ загрузки и образ результата.</span><span class="sxs-lookup"><span data-stu-id="e375d-156">This object includes all tracks, and references to the boot image and result image.</span></span>
<ul>
<li><span data-ttu-id="e375d-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>дфилесистемимажеевентс</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></span></span></li>
<li><span data-ttu-id="e375d-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>дфилесистемимажеимпортевентс</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></span></span></li>
<li><span data-ttu-id="e375d-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>ифилесистемимаже</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></span></span></li>
<li><span data-ttu-id="e375d-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span></span></li>
<li><span data-ttu-id="e375d-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-162">кфилесистемимаже</span><span class="sxs-lookup"><span data-stu-id="e375d-162">CFileSystemImage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-163">Контейнер потока данных, предоставленный объектом файловой системы.</span><span class="sxs-lookup"><span data-stu-id="e375d-163">Container of the data stream provided by the file system object.</span></span>
<ul>
<li><span data-ttu-id="e375d-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>ифилесистемимажересулт</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-165">филесистемимажересулт</span><span class="sxs-lookup"><span data-stu-id="e375d-165">FileSystemImageResult</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-166">Элемент каталога в образе файловой системы.</span><span class="sxs-lookup"><span data-stu-id="e375d-166">Directory item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="e375d-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>ифсидиректоритем</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></span></span></li>
<li><span data-ttu-id="e375d-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-169">фсидиректоритем</span><span class="sxs-lookup"><span data-stu-id="e375d-169">FsiDirectoryItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-170">Файловый элемент в образе файловой системы.</span><span class="sxs-lookup"><span data-stu-id="e375d-170">File item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="e375d-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>ифсифилеитем</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></span></span></li>
<li><span data-ttu-id="e375d-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-173">фсифилеитем</span><span class="sxs-lookup"><span data-stu-id="e375d-173">FsiFileItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-174">Интерфейс, содержащий свойства, общие для файлов и элементов каталога.</span><span class="sxs-lookup"><span data-stu-id="e375d-174">Interface containing properties common to both file and directory items.</span></span>
<ul>
<li><span data-ttu-id="e375d-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>ифсиитем</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-176">фсиитем</span><span class="sxs-lookup"><span data-stu-id="e375d-176">FsiItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-177">Создание необработанного образа компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="e375d-177">RAW CD image creation.</span></span>
<ul>
<li><span data-ttu-id="e375d-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>иравкдимажекреатор</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></span></span></li>
<li><span data-ttu-id="e375d-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>иравкдимажетраккинфо</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-180">мсфтравкдимажекреатор</span><span class="sxs-lookup"><span data-stu-id="e375d-180">MsftRawCDImageCreator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-181">Объект модуля поддержки объекта Stream для сцепления нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="e375d-181">Stream object helper object to concatenate multiple streams.</span></span>
<ul>
<li><span data-ttu-id="e375d-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>истреамконкатенате</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-183">мсфтстреамконкатенате</span><span class="sxs-lookup"><span data-stu-id="e375d-183">MsftStreamConcatenate</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-184">Поток с чередованием для добавления к образу диска.</span><span class="sxs-lookup"><span data-stu-id="e375d-184">Interleaved stream to add to the disc image.</span></span>
<ul>
<li><span data-ttu-id="e375d-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>истреаминтерлеаве</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-186">мсфтстреаминтерлеаве</span><span class="sxs-lookup"><span data-stu-id="e375d-186">MsftStreamInterleave</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-187">Созданный в псевдо-Random поток.</span><span class="sxs-lookup"><span data-stu-id="e375d-187">Pseudo-random generated stream.</span></span>
<ul>
<li><span data-ttu-id="e375d-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>истреампсеудорандомбасед</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-189">MsftStreamPrgn001</span><span class="sxs-lookup"><span data-stu-id="e375d-189">MsftStreamPrgn001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-190">Объект скрипта <strong>мсфтстреамзеро</strong> не реализован в качестве интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e375d-190">The <strong>MsftStreamZero</strong> scripting object is not implemented as an interface.</span></span></td>
<td><span data-ttu-id="e375d-191"><a href="msftstreamzero.md"><strong>мсфтстреамзеро</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-191"><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e375d-192">В следующей таблице перечислены вспомогательные интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="e375d-192">The following table lists helper interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e375d-193">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="e375d-193">Interface</span></span></td>
<td><span data-ttu-id="e375d-194">Объект</span><span class="sxs-lookup"><span data-stu-id="e375d-194">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-195">Коллекция диапазонов секторов в образе файловой системы.</span><span class="sxs-lookup"><span data-stu-id="e375d-195">Collection of sector ranges within a file system image.</span></span>
<ul>
<li><span data-ttu-id="e375d-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>иблоккранже</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></span></span></li>
<li><span data-ttu-id="e375d-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>иблоккранжелист</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-198">Нет соответствующего объекта</span><span class="sxs-lookup"><span data-stu-id="e375d-198">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-199">Поддержка записи при проверке.</span><span class="sxs-lookup"><span data-stu-id="e375d-199">Burn verification support.</span></span>
<ul>
<li><span data-ttu-id="e375d-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>ибурнверификатион</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-201">Нет соответствующего объекта</span><span class="sxs-lookup"><span data-stu-id="e375d-201">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-202">Перечислитель Фсиитемс для приложений C/C++.</span><span class="sxs-lookup"><span data-stu-id="e375d-202">Enumerator of FsiItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="e375d-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>иенумфсиитемс</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-204">енумфсиитемс</span><span class="sxs-lookup"><span data-stu-id="e375d-204">EnumFsiItems</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-205">Перечислитель Прогресситемс для приложений C/C++.</span><span class="sxs-lookup"><span data-stu-id="e375d-205">Enumerator of ProgressItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="e375d-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>иенумпрогресситемс</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-207">енумпрогресситемс</span><span class="sxs-lookup"><span data-stu-id="e375d-207">EnumProgressItems</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="e375d-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>ифсинамедстреамс</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-209">FsiFileItem2</span><span class="sxs-lookup"><span data-stu-id="e375d-209">FsiFileItem2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-210">Поддержка проверки ISO-образа.</span><span class="sxs-lookup"><span data-stu-id="e375d-210">.iso image verification support.</span></span>
<ul>
<li><span data-ttu-id="e375d-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>иисоимажеманажер</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-212">Нет соответствующего объекта</span><span class="sxs-lookup"><span data-stu-id="e375d-212">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-213">Поддержка нескольких сеансов.</span><span class="sxs-lookup"><span data-stu-id="e375d-213">Multiple session support.</span></span>
<ul>
<li><span data-ttu-id="e375d-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>имултисессион</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-215">Нет соответствующего объекта</span><span class="sxs-lookup"><span data-stu-id="e375d-215">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-216">Последовательная поддержка нескольких сеансов.</span><span class="sxs-lookup"><span data-stu-id="e375d-216">Sequential multiple session support.</span></span>
<ul>
<li><span data-ttu-id="e375d-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>имултисессионсекуентиал</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></span></span></li>
<li><span data-ttu-id="e375d-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-219">мсфтмултисессионсекуентиал</span><span class="sxs-lookup"><span data-stu-id="e375d-219">MsftMultisessionSequential</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e375d-220">Имя файла и связанные блоки в результирующем изображении.</span><span class="sxs-lookup"><span data-stu-id="e375d-220">File name and associated blocks in the result image.</span></span>
<ul>
<li><span data-ttu-id="e375d-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>ипрогресситем</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-222">прогресситем</span><span class="sxs-lookup"><span data-stu-id="e375d-222">ProgressItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e375d-223">Вывод образа результатов, разбитый по имени файла и связанным блокам.</span><span class="sxs-lookup"><span data-stu-id="e375d-223">Result image listing, broken down by file name and associated blocks.</span></span>
<ul>
<li><span data-ttu-id="e375d-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>ипрогресситемс</strong></a></span><span class="sxs-lookup"><span data-stu-id="e375d-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="e375d-225">прогресситемс</span><span class="sxs-lookup"><span data-stu-id="e375d-225">ProgressItems</span></span></td>
</tr>
</tbody>
</table>



 

 

 




