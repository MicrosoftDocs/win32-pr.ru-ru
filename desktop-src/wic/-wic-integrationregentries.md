---
description: Этот раздел относится к Windows Vista и более поздним версиям.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: Интеграция с Фотоальбомом Windows и проводником Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ab2bb725b151a069f53a94a8fb2e31766132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647485"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a><span data-ttu-id="89666-103">Интеграция с Фотоальбомом Windows и проводником Windows</span><span class="sxs-lookup"><span data-stu-id="89666-103">Integration with Windows Photo Gallery and Windows Explorer</span></span>

<span data-ttu-id="89666-104">Этот раздел относится к Windows Vista и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="89666-104">This topic applies to Windows Vista and later.</span></span> <span data-ttu-id="89666-105">Он содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="89666-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="89666-106">Введение</span><span class="sxs-lookup"><span data-stu-id="89666-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="89666-107">Интеграция с хранилищем свойств Windows</span><span class="sxs-lookup"><span data-stu-id="89666-107">Integration with the Windows Property Store</span></span>](#integration-with-the-windows-property-store)
-   [<span data-ttu-id="89666-108">Интеграция с Фотоальбомом Windows</span><span class="sxs-lookup"><span data-stu-id="89666-108">Integration with the Windows Photo Gallery</span></span>](#integration-with-the-windows-photo-gallery)
-   [<span data-ttu-id="89666-109">Интеграция с кэшем эскизов Windows</span><span class="sxs-lookup"><span data-stu-id="89666-109">Integration with the Windows Thumbnail Cache</span></span>](#integration-with-the-windows-thumbnail-cache)
-   [<span data-ttu-id="89666-110">См. также</span><span class="sxs-lookup"><span data-stu-id="89666-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="89666-111">Введение</span><span class="sxs-lookup"><span data-stu-id="89666-111">Introduction</span></span>

<span data-ttu-id="89666-112">Чтобы включить в фотоальбоме Windows и проводнике Windows отображение эскизов и поиск и обновление метаданных стандартного образа, кодек должен иметь связанную с ним реализацию интерфейсов [исумбнаилпровидер](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) и [ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="89666-112">To enable Windows Photo Gallery and Windows Explorer to display thumbnails and search and update standard image metadata, a codec must have an implementation of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) and [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces associated with it.</span></span> <span data-ttu-id="89666-113">Интерфейс Исумбнаилпровидер используется для получения эскизов и заполнения кэша эскизов, а интерфейс Ипропертисторе используется для поиска и обновления метаданных, связанных с файлом.</span><span class="sxs-lookup"><span data-stu-id="89666-113">The IThumbnailProvider interface is used to retrieve thumbnails and populate the thumbnail cache, and the IPropertyStore interface is used for searching and updating metadata associated with a file.</span></span> <span data-ttu-id="89666-114">Начиная с Windows Vista, все типы файлов имеют эскизы и метаданные, но для разных типов файлов требуются разные реализации этих интерфейсов для извлечения или создания эскизов и метаданных для них.</span><span class="sxs-lookup"><span data-stu-id="89666-114">As of Windows Vista, all file types have thumbnails and metadata, but different file types require different implementations of these interfaces to retrieve or generate the thumbnails and metadata for them.</span></span> <span data-ttu-id="89666-115">Система предоставляет реализации по умолчанию этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="89666-115">The system provides default implementations of these interfaces.</span></span> <span data-ttu-id="89666-116">Реализация Исумбнаилпровидер по умолчанию может использоваться для любого формата изображения, поддерживающего Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="89666-116">The default implementation of IThumbnailProvider can be used for any Windows Imaging Component (WIC)–enabled image format.</span></span> <span data-ttu-id="89666-117">Реализация Ипропертисторе по умолчанию может использоваться с любым форматом изображений с поддержкой WIC, основанным на формате TIFF или в контейнере JPEG.</span><span class="sxs-lookup"><span data-stu-id="89666-117">The default implementation of IPropertyStore can be used with any WIC-enabled image format that is based on a Tagged Image File Format (TIFF) or JPEG container.</span></span> <span data-ttu-id="89666-118">Чтобы связать формат изображения с реализациями по умолчанию обоих интерфейсов, необходимо добавить лишь несколько записей реестра.</span><span class="sxs-lookup"><span data-stu-id="89666-118">To associate your image format with the default implementations of both of these interfaces, you must add just a few registry entries.</span></span>

<span data-ttu-id="89666-119">Следующие записи указывают на Фотоальбом Windows и проводник Windows, что расширение имени файла (EXT) и связанный с ним тип MIME связаны с форматом изображения.</span><span class="sxs-lookup"><span data-stu-id="89666-119">The following entries indicate to the Windows Photo Gallery and Windows Explorer that a file name extension (.ext) and its associated MIME type are associated with an image format.</span></span>

<span data-ttu-id="89666-120">Следующая запись обозначает Windows и приложения, использующие тип содержимого (также известный как тип MIME), что файл с заданным расширением (EXT) имеет формат изображения.</span><span class="sxs-lookup"><span data-stu-id="89666-120">The following entry indicates to Windows and applications that use content type (also known as mime type) that a file with a given extension (.ext) is an image format.</span></span> <span data-ttu-id="89666-121">Владелец типа файла должен выбрать `<image sub type value>` , который однозначно определяет формат файла, и это значение типа содержимого должно быть зарегистрировано в IANA.</span><span class="sxs-lookup"><span data-stu-id="89666-121">The file type owner needs to choose a `<image sub type value>` that uniquely identifies the file format and this content type value needs to be register with IANA.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

<span data-ttu-id="89666-122">Следующая запись обозначает Windows, Поиск Windows и приложения, использующие [System. Kind](../properties/props-system-kind.md) , что расширение имени файла (EXT) должно рассматриваться как изображение.</span><span class="sxs-lookup"><span data-stu-id="89666-122">The following entry indicates to Windows, Windows search and applications that use [System.Kind](../properties/props-system-kind.md) that a file name extension (.ext) should be treated as a picture.</span></span> <span data-ttu-id="89666-123">В частности, это означает, что свойству System. Kind расширения файла должно быть присвоено значение Picture.</span><span class="sxs-lookup"><span data-stu-id="89666-123">Specifically, it indicates that the file extension’s System.Kind property should be set to Picture.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     {.ext} = Picture
```

## <a name="integration-with-the-windows-property-store"></a><span data-ttu-id="89666-124">Интеграция с хранилищем свойств Windows</span><span class="sxs-lookup"><span data-stu-id="89666-124">Integration with the Windows Property Store</span></span>

<span data-ttu-id="89666-125">Иногда одни и те же свойства метаданных предоставляются в разных схемах метаданных, часто с разными именами свойств.</span><span class="sxs-lookup"><span data-stu-id="89666-125">Sometimes the same metadata properties are exposed in different metadata schemas, often with different property names.</span></span> <span data-ttu-id="89666-126">Когда одно из этих свойств обновляется, но другие — нет, метаданные в файле могут оказаться несинхронизированными. Обработчик свойств Photo предоставляет **ипропертисторе** реализацию по умолчанию для изображений и используется приложениями, а также фотоальбомом Windows и проводником Windows, чтобы гарантировать синхронизацию всех метаданных в образе и отображение свойств, отображаемых приложениями, в фотоальбоме Windows и проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="89666-126">When one of these properties is updated, but the others are not, the metadata within the file can get out of sync. The photo property handler provides the default **IPropertyStore** implementation for images, and is used by applications as well as by the Windows Photo Gallery and Windows Explorer to ensure that all the metadata in an image stays in sync, and that the properties displayed by applications are consistent with those displayed by the Windows Photo Gallery and Windows Explorer.</span></span> <span data-ttu-id="89666-127">Когда обработчик свойства Photo обновляет метаданные, гарантируется согласованность этих свойств по всем общим форматам метаданных, присутствующим в файле.</span><span class="sxs-lookup"><span data-stu-id="89666-127">When the photo property handler updates metadata, it makes sure that these properties are updated consistently across all the common metadata formats that are present in the file.</span></span>

<span data-ttu-id="89666-128">Обработчик свойства Photo должен понимать формат контейнера и способ определения различных свойств в нем.</span><span class="sxs-lookup"><span data-stu-id="89666-128">The photo property handler must understand the container format and how to locate the various properties within it.</span></span> <span data-ttu-id="89666-129">В целом, обработчик свойства Photo не может узнать, как различные блоки метаданных размещаются в собственном формате контейнера.</span><span class="sxs-lookup"><span data-stu-id="89666-129">In general, it isn’t possible for the photo property handler to know how the various metadata blocks are laid out in a proprietary container format.</span></span> <span data-ttu-id="89666-130">Однако если метаданные в вашем формате контейнера размещаются так же, как метаданные в формате контейнера TIFF или в формате контейнера JPEG, то обработчик свойства Photo может воспользоваться этими знаниями для согласованного обновления метаданных в вашем формате контейнера.</span><span class="sxs-lookup"><span data-stu-id="89666-130">However, if the metadata in your container format is laid out the same way as the metadata in either a TIFF container format or a JPEG container format, the photo property handler can take advantage of that knowledge to update metadata consistently in your container format as well.</span></span>

<span data-ttu-id="89666-131">Эту связь можно зарегистрировать, создав следующую запись реестра.</span><span class="sxs-lookup"><span data-stu-id="89666-131">You can register this association by creating the following registry entry.</span></span> <span data-ttu-id="89666-132">Эта запись сообщает обработчику свойства Photo, что формат контейнера, идентифицируемый этим идентификатором GUID, распознает те же пути языка запросов метаданных, что и формат контейнера с идентификатором GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3.</span><span class="sxs-lookup"><span data-stu-id="89666-132">This entry notifies the photo property handler that the container format identified by this GUID understands the same metadata query language paths as the container format with the GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3.</span></span> <span data-ttu-id="89666-133">(163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 — это идентификатор GUID для формата контейнера TIFF.)</span><span class="sxs-lookup"><span data-stu-id="89666-133">(163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 is the GUID for the TIFF container format.)</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  ContainerAssociations
                     {Container Format GUID} = {163bcc30-e2e9-4f0b-961d-a3e9fdb788a3}
```

<span data-ttu-id="89666-134">Следующая запись связывает стандартную реализацию **ипропертисторе** обработчика свойства Photo с файлами с расширением ext.</span><span class="sxs-lookup"><span data-stu-id="89666-134">The following entry associates the photo property handler’s default implementation of **IPropertyStore** with files that have the extension ".ext".</span></span> <span data-ttu-id="89666-135">Первым идентификатором GUID является IID интерфейса **ипропертисторе** , а вторым — идентификатор GUID его реализации обработчика свойства Photo.</span><span class="sxs-lookup"><span data-stu-id="89666-135">The first GUID is the IID of the **IPropertyStore** interface, and the second is the GUID of the photo property handler’s implementation of it.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  {.ext}
                     (Default) = {a38b883c-1682-497e-97b0-0a3a9e801682}
```

<span data-ttu-id="89666-136">Кодеки, использующие собственный формат, несовместимый с форматом контейнера TIFF или JPEG, должны записывать собственную реализацию **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="89666-136">Codecs that use a proprietary format that is not compatible with either the TIFF or JPEG container format must write their own **IPropertyStore** implementation.</span></span>

## <a name="integration-with-the-windows-photo-gallery"></a><span data-ttu-id="89666-137">Интеграция с Фотоальбомом Windows</span><span class="sxs-lookup"><span data-stu-id="89666-137">Integration with the Windows Photo Gallery</span></span>

<span data-ttu-id="89666-138">Фотоальбом Windows построен на основе WIC и может отображать любой формат изображений с поддержкой WIC, для которого установлен кодек.</span><span class="sxs-lookup"><span data-stu-id="89666-138">Windows Photo Gallery is built on WIC and can display any WIC-enabled image format for which the codec is installed.</span></span> <span data-ttu-id="89666-139">Чтобы уведомить систему о том, что ваш формат изображения можно открыть в фотоальбоме Windows, необходимо создать сопоставление файлов, создав следующие записи реестра.</span><span class="sxs-lookup"><span data-stu-id="89666-139">To notify the system that your image format can be opened in Windows Photo Gallery, you need to create a file association by creating the following registry entries.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      (Default) = {ProgID} for example, jpegfile)
      OpenWithProgids
         {ProgID}
      OpenWithList
         PhotoViewer.dll
      ShellEx
         ContextMenuHandlers
            ShellImagePreview
               (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   SystemFileAssociations
      {.ext}
         OpenWithList
            PhotoViewer.dll
         ShellEx
            ContextMenuHandlers
               ShellImagePreview
                  (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   {Image Format ProgID}
      (Default) = Name of Image Format
      DefaultIcon
         (Default) = Path to icon for type, icon index
      shell
         open
            MuiVerb = @%PROGRAMFILES%\Windows Photo Gallery\photoviewer.dll,-3043
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%ProgramFiles%\Windows Photo Gallery\PhotoViewer.dll", ImageView_Fullscreen %1
            DropTarget
               Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
         printo
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%SystemRoot%\System32\shimgvw.dll", ImageView_PrintTo /pt "%1" "%2" "%3" "%4"
```

<span data-ttu-id="89666-140">ProgID обычно является расширением имени файла, к которому добавляется слово «File».</span><span class="sxs-lookup"><span data-stu-id="89666-140">The ProgID is usually the file name extension appended with the word "file".</span></span> <span data-ttu-id="89666-141">(Например, если расширение имени файла — txt, ProgID обычно имеет значение "ткстфиле".)</span><span class="sxs-lookup"><span data-stu-id="89666-141">(For example, if the file name extension is .txt, the ProgID would usually be "txtfile".)</span></span>

<span data-ttu-id="89666-142">Существуют и другие стандартные записи реестра, которые может потребоваться создать для поддержки сопоставлений файлов. Однако, поскольку се'и не относятся к WIC, они выходят за рамки данного раздела.</span><span class="sxs-lookup"><span data-stu-id="89666-142">There are other standard registry entries you may need to create to support file associations; however, because the’y are not specific to WIC, they are beyond the scope of this topic.</span></span>

## <a name="integration-with-the-windows-thumbnail-cache"></a><span data-ttu-id="89666-143">Интеграция с кэшем эскизов Windows</span><span class="sxs-lookup"><span data-stu-id="89666-143">Integration with the Windows Thumbnail Cache</span></span>

<span data-ttu-id="89666-144">Следующие две записи указывают, что стандартную реализацию поставщика снимков WIC можно использовать для получения эскизов файлов с этим расширением.</span><span class="sxs-lookup"><span data-stu-id="89666-144">The following two entries indicate that the standard WIC thumbnail provider implementation can be used to retrieve thumbnails for files with this extension.</span></span> <span data-ttu-id="89666-145">Первым идентификатором GUID является IID интерфейса [исумбнаилпровидер](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) , а вторым — идентификатор GUID стандартной системной реализации этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="89666-145">The first GUID is the IID of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) interface, and the second is the GUID of the standard system implementation of this interface.</span></span> <span data-ttu-id="89666-146">(Все записи в ХЛКР \\ . ext \\ шеллекс \\ повторяются в разделе HKCR \\ системфилеассоЦиатионс \\ . ext \\ шеллекс \\ .)</span><span class="sxs-lookup"><span data-stu-id="89666-146">(All entries under HLCR\\.ext\\ShellEx\\ are repeated under HKCR\\SystemFileAssociations\\.ext\\ShellEx\\.)</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a><span data-ttu-id="89666-147">См. также</span><span class="sxs-lookup"><span data-stu-id="89666-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="89666-148">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="89666-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="89666-149">Записи реестра, относящиеся к кодировщику</span><span class="sxs-lookup"><span data-stu-id="89666-149">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="89666-150">Установка и регистрация КОДЕка</span><span class="sxs-lookup"><span data-stu-id="89666-150">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="89666-151">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="89666-151">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="89666-152">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="89666-152">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
