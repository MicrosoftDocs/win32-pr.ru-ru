---
description: Файлы описания библиотеки — это XML-файлы, определяющие библиотеки.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Схема описания библиотеки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bebbd7ed168cd977530ccfeb0b319c33142687
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104986192"
---
# <a name="library-description-schema"></a><span data-ttu-id="b232c-103">Схема описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="b232c-103">Library Description Schema</span></span>

<span data-ttu-id="b232c-104">Файлы описания библиотеки — это XML-файлы, определяющие библиотеки.</span><span class="sxs-lookup"><span data-stu-id="b232c-104">Library description files are XML files that define libraries.</span></span> <span data-ttu-id="b232c-105">Библиотеки объединяют элементы из локальных и удаленных мест хранения в единое представление в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="b232c-105">Libraries aggregate items from local and remote storage locations into a single view in Windows Explorer.</span></span> <span data-ttu-id="b232c-106">Файлы описания библиотеки соответствуют схеме описания библиотеки и сохраняются в \* файлах. Library-MS.</span><span class="sxs-lookup"><span data-stu-id="b232c-106">Library description files follow the Library Description schema and are saved as \*.library-ms files.</span></span>

<span data-ttu-id="b232c-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="b232c-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b232c-108">Общие сведения о схеме описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="b232c-108">Overview of the Library Description Schema</span></span>](#overview-of-the-library-description-schema)
-   [<span data-ttu-id="b232c-109">Управление версиями пространства имен</span><span class="sxs-lookup"><span data-stu-id="b232c-109">Namespace Versioning</span></span>](#namespace-versioning)
-   [<span data-ttu-id="b232c-110">Пример файла описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="b232c-110">Example of a Library Description File</span></span>](#example-of-a-library-description-file)
-   [<span data-ttu-id="b232c-111">См. также</span><span class="sxs-lookup"><span data-stu-id="b232c-111">Related topics</span></span>](#related-topics)

## <a name="overview-of-the-library-description-schema"></a><span data-ttu-id="b232c-112">Общие сведения о схеме описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="b232c-112">Overview of the Library Description Schema</span></span>

<span data-ttu-id="b232c-113">Библиотеки содержат файлы, которые хранятся в одном или нескольких местах хранения.</span><span class="sxs-lookup"><span data-stu-id="b232c-113">Libraries contain files that are stored in one or more storage locations.</span></span> <span data-ttu-id="b232c-114">Библиотеки на самом деле не хранят эти файлы; Вместо этого они отслеживают папки, содержащие файлы, и предоставляют пользователям доступ к файлам и их упорядочение различными способами.</span><span class="sxs-lookup"><span data-stu-id="b232c-114">Libraries do not actually store these files; instead, they monitor the folders that contain the files, and let users access and arrange the files in different ways.</span></span> <span data-ttu-id="b232c-115">Например, пользователь может иметь музыкальные файлы в нескольких папках на локальном жестком диске, а также на внешнем жестком диске.</span><span class="sxs-lookup"><span data-stu-id="b232c-115">For example, a user can have music files in multiple folders on a local hard disk and also on an external hard disk.</span></span> <span data-ttu-id="b232c-116">С помощью **библиотеки музыки** пользователь может одновременно получить доступ ко всем файлам и отсортировать их по имени исполнителя или названию альбома в виде одной группы.</span><span class="sxs-lookup"><span data-stu-id="b232c-116">Using the **Music Library**, the user can access all of those files at the same time and sort them all by artist name or album title as a single group.</span></span>

<span data-ttu-id="b232c-117">Схема описания библиотеки состоит из трех основных частей, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b232c-117">The Library Description schema consists of three major parts, described in the following table:</span></span>



|                             |                                                                                                                                                            |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b232c-118">Общие сведения о библиотеке</span><span class="sxs-lookup"><span data-stu-id="b232c-118">General library information</span></span> | <span data-ttu-id="b232c-119">Сведения о библиотеке, такие как имя, владелец, версия, значок, который может использоваться проводником Windows при отображении библиотеки для пользователя.</span><span class="sxs-lookup"><span data-stu-id="b232c-119">Information about the library, such as name, owner, version, icon, that Windows Explorer can use when it displays the library to a user.</span></span>                   |
| <span data-ttu-id="b232c-120">Свойства библиотеки</span><span class="sxs-lookup"><span data-stu-id="b232c-120">Library properties</span></span>          | <span data-ttu-id="b232c-121">Одно или несколько свойств, описывающих библиотеку.</span><span class="sxs-lookup"><span data-stu-id="b232c-121">One or more properties that describe the library.</span></span> <span data-ttu-id="b232c-122">Эти пользовательские свойства относятся к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="b232c-122">These custom properties are specific to the library.</span></span>                                                     |
| <span data-ttu-id="b232c-123">Расположения библиотек</span><span class="sxs-lookup"><span data-stu-id="b232c-123">Library locations</span></span>           | <span data-ttu-id="b232c-124">Один или несколько соединителей поиска, которые указывают места хранения для включения в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="b232c-124">One or more search connectors that identify storage locations to include in the library.</span></span> <span data-ttu-id="b232c-125">Каждое из этих расположений также может иметь уникальный набор свойств.</span><span class="sxs-lookup"><span data-stu-id="b232c-125">Each of these locations can also have a unique set of properties.</span></span> |



 

<span data-ttu-id="b232c-126">Файлы библиотек в Windows 7 хранятся в известной папке FOLDERID \_ Library.</span><span class="sxs-lookup"><span data-stu-id="b232c-126">Library files in Windows 7 are stored in the known folder, FOLDERID\_Libraries.</span></span> <span data-ttu-id="b232c-127">По умолчанию папка FOLDERID \_ Libraries находится в каталоге% UserProfile% \\ AppData \\ роуминга \\ \\ библиотеки Microsoft Windows \\ .</span><span class="sxs-lookup"><span data-stu-id="b232c-127">By default, the FOLDERID\_Libraries folder is located at %USERPROFILE%\\AppData\\Roaming\\Microsoft\\Windows\\Libraries.</span></span>

## <a name="namespace-versioning"></a><span data-ttu-id="b232c-128">Управление версиями пространства имен</span><span class="sxs-lookup"><span data-stu-id="b232c-128">Namespace Versioning</span></span>

<span data-ttu-id="b232c-129">Версии формата файла описания библиотеки ( \* . Library-MS) отправляются путем изменения пространства имен.</span><span class="sxs-lookup"><span data-stu-id="b232c-129">Versions of the Library Description file format (\*.library-ms) are tracked by changing the namespace.</span></span> <span data-ttu-id="b232c-130">В Windows 7 формат файла имеет следующее пространство имен по умолчанию: https://schemas.microsoft.com/windows/2009/library .</span><span class="sxs-lookup"><span data-stu-id="b232c-130">For Windows 7, the file format has the following default namespace: https://schemas.microsoft.com/windows/2009/library.</span></span>

<span data-ttu-id="b232c-131">Однако версии содержимого библиотеки отправляются с помощью [<version>](schema-library-version.md) элемента в указанном файле описания библиотеки.</span><span class="sxs-lookup"><span data-stu-id="b232c-131">Versions of the library contents, however, are tracked by using the [<version>](schema-library-version.md) element in a specific Library Description file.</span></span>

## <a name="example-of-a-library-description-file"></a><span data-ttu-id="b232c-132">Пример файла описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="b232c-132">Example of a Library Description File</span></span>

<span data-ttu-id="b232c-133">Ниже приведен пример файла описания библиотеки, который определяет библиотеку для файлов документов.</span><span class="sxs-lookup"><span data-stu-id="b232c-133">The following is an example of a Library Description file that defines a library for document files.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a><span data-ttu-id="b232c-134">См. также</span><span class="sxs-lookup"><span data-stu-id="b232c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b232c-135">Элемент Фолдертипе (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="b232c-135">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="b232c-136">Элемент Иконреференце (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="b232c-136">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="b232c-137">Элемент Ислибрарипиннед (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="b232c-137">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="b232c-138">Элемент Либраридескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="b232c-138">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="b232c-139">Элемент Name (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="b232c-139">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="b232c-140">Элемент ownerSID (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="b232c-140">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="b232c-141">Элемент Property (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="b232c-141">property Element (Library Schema)</span></span>](schema-library-property.md)
</dt> <dt>

[<span data-ttu-id="b232c-142">Элемент Пропертисторе (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="b232c-142">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="b232c-143">Элемент Сеарчконнектордескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="b232c-143">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="b232c-144">Элемент Сеарчконнектордескриптионлист (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="b232c-144">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="b232c-145">Элемент Темплатеинфо (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="b232c-145">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="b232c-146">Элемент Version (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="b232c-146">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> <dt>

[<span data-ttu-id="b232c-147">Схема описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="b232c-147">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
