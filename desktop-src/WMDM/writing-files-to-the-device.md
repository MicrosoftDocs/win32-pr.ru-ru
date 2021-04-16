---
title: Запись файлов на устройство
description: Запись файлов на устройство
ms.assetid: 66eaed16-032b-4ac0-a768-aded80f10255
keywords:
- Диспетчер устройств Windows Media, запись файлов на устройства
- Диспетчер устройств, запись файлов на устройства
- руководства по программированию, запись файлов на устройства
- Классические приложения, запись файлов на устройства
- Создание приложений диспетчер устройств Windows Media, запись файлов на устройства
- запись файлов на устройства, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d8b5234cc275eed1b4aa344c16a2b927b8122d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531886"
---
# <a name="writing-files-to-the-device"></a><span data-ttu-id="48909-109">Запись файлов на устройство</span><span class="sxs-lookup"><span data-stu-id="48909-109">Writing Files to the Device</span></span>

<span data-ttu-id="48909-110">Перед отправкой файла на устройство приложение должно выяснить, какие типы файлов и форматы могут обрабатываться устройством, чтобы приложение могла определить, должен ли файл быть перекодирован перед отправкой или отправкой неизмененных или вообще не отправляться.</span><span class="sxs-lookup"><span data-stu-id="48909-110">Before sending a file to a device, your application must find out what types of files and formats the device can handle, so that the application can determine whether the file should be transcoded before sending, or sent unmodified, or not sent at all.</span></span>

<span data-ttu-id="48909-111">В следующих шагах показано, как отправить существующий файл на устройство.</span><span class="sxs-lookup"><span data-stu-id="48909-111">The following steps show how to send an existing file down to the device.</span></span> <span data-ttu-id="48909-112">Сведения о создании нового файла на устройстве, например списка воспроизведения, см. в разделе [Создание списка воспроизведения на устройстве](creating-a-playlist-on-the-device.md).</span><span class="sxs-lookup"><span data-stu-id="48909-112">To create a new file on the device, such as a playlist, see [Creating a Playlist on the Device](creating-a-playlist-on-the-device.md).</span></span>

1.  <span data-ttu-id="48909-113">Получите формат файла, который планируется отправить на устройство.</span><span class="sxs-lookup"><span data-stu-id="48909-113">Get the format of the file you intend to send to the device.</span></span> <span data-ttu-id="48909-114">Дополнительные сведения см. [в разделе Обнаружение формата файла](discovering-a-files-format.md).</span><span class="sxs-lookup"><span data-stu-id="48909-114">For more information, see [Discovering a File's Format](discovering-a-files-format.md).</span></span>
2.  <span data-ttu-id="48909-115">Если устройство предназначено для воспроизведения файла,</span><span class="sxs-lookup"><span data-stu-id="48909-115">If the device is intended to play the file,</span></span>
    -   <span data-ttu-id="48909-116">Запросите у файла возможности его форматирования.</span><span class="sxs-lookup"><span data-stu-id="48909-116">Query the file for its format capabilities.</span></span> <span data-ttu-id="48909-117">Дополнительные сведения см. в разделе [Обнаружение возможностей форматирования устройств](discovering-device-format-capabilities.md).</span><span class="sxs-lookup"><span data-stu-id="48909-117">For more information, see [Discovering Device Format Capabilities](discovering-device-format-capabilities.md).</span></span>
    -   <span data-ttu-id="48909-118">Найдите допустимый формат, который приложение может создать из исходного файла.</span><span class="sxs-lookup"><span data-stu-id="48909-118">Find an acceptable format that the application can create from the original file.</span></span>
    -   <span data-ttu-id="48909-119">Если файл необходимо перекодировать, перекодировать его.</span><span class="sxs-lookup"><span data-stu-id="48909-119">If the file needs to be transcoded, transcode it.</span></span>
3.  <span data-ttu-id="48909-120">Найти родительское хранилище для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="48909-120">Find a parent storage for the new object.</span></span> <span data-ttu-id="48909-121">Диспетчер устройств Windows Media не предоставляет способ обнаружения стандартного расположения хранилища для определенных типов файлов (видео-или звуковых файлов, WMV или BMP, папки "Избранное" и т. д.), поэтому необходимо изучить каждое устройство, чтобы выяснить, где лучше всего хранить новый объект.</span><span class="sxs-lookup"><span data-stu-id="48909-121">Windows Media Device Manager does not provide a way to discover the standard storage location for any particular file types (video or audio files, WMV or BMP, a "Favorites" folder, and so on), so you will have to examine each device to try to figure out where best to store the new object.</span></span> <span data-ttu-id="48909-122">(В других приложениях применяется определенная структура папок, например проигрыватель Windows Media создает альбомы, списки воспроизведения и музыкальные папки, в которых папка Music содержит исполнителя и Албумнаме иерархии.</span><span class="sxs-lookup"><span data-stu-id="48909-122">(Other applications enforce a certain folder structure, for example, Windows Media Player creates Albums, Playlists and Music folders where the Music folder contains an Artist and AlbumName heirarchy.</span></span> <span data-ttu-id="48909-123">По этой причине, так как некоторые устройства могут не проверяться с помощью программного обеспечения, отличного от проигрывателя Windows Media, следует помнить, что размещение списков воспроизведения или объектов альбома в любой папке, кроме списков воспроизведения или альбомов, иногда может привести к неработоспособности объектов на некоторых устройствах.)</span><span class="sxs-lookup"><span data-stu-id="48909-123">For this reason, and because some devices may not have been tested with software other than Windows Media Player, be aware that the placement of playlist or album objects in any folder other than the Playlists or Albums folders may sometimes lead to nonfunctioning objects on some devices.)</span></span>
4.  <span data-ttu-id="48909-124">Если целевое хранилище поддерживает [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3), создайте новый интерфейс метаданных, вызвав [**IWMDMStorage3:: креатимптиметадатаобжект**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span><span class="sxs-lookup"><span data-stu-id="48909-124">If the target storage supports [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3), create a new metadata interface by calling [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span></span> <span data-ttu-id="48909-125">Задайте метаданные в интерфейсе [**ивмдмметадата**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) .</span><span class="sxs-lookup"><span data-stu-id="48909-125">Set metadata on an [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) interface.</span></span> <span data-ttu-id="48909-126">Дополнительные сведения см. [в разделе Установка метаданных для файла](setting-metadata-on-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="48909-126">For more information, see [Setting Metadata on a File](setting-metadata-on-a-file.md).</span></span> <span data-ttu-id="48909-127">Единственными обязательными метаданными являются g \_ всзвмдмформаткоде (значение [**вмдм \_ форматкоде**](wmdm-formatcode.md) , описывающее содержимое), но чем больше метаданных вы можете предоставить, тем эффективнее будет перемещение для поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="48909-127">The only required metadata is g\_wszWMDMFormatCode (a [**WMDM\_FORMATCODE**](wmdm-formatcode.md) value describing the content), but the more metadata you can provide, the more efficient the transfer will be for the service provider.</span></span>
5.  <span data-ttu-id="48909-128">Отправьте файл на устройство с помощью метода [**INSERT**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)или [**Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) .</span><span class="sxs-lookup"><span data-stu-id="48909-128">Send the file to the device by using the [**Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2), or [**Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) method.</span></span> <span data-ttu-id="48909-129">**Insert3** позволяет включить метаданные на устройстве как часть метода.</span><span class="sxs-lookup"><span data-stu-id="48909-129">**Insert3** allows you to include the metadata on the device as part of the method.</span></span> <span data-ttu-id="48909-130">Дополнительные сведения см. в разделе [Отправка файла на устройство](sending-the-file-to-the-device.md).</span><span class="sxs-lookup"><span data-stu-id="48909-130">For more information, see [Sending the File to the Device](sending-the-file-to-the-device.md).</span></span>

<span data-ttu-id="48909-131">Код, демонстрирующий каждое из этих действий, приведен на страницах связанных разделов.</span><span class="sxs-lookup"><span data-stu-id="48909-131">Code demonstrating each of these steps is provided on the linked topic pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48909-132">См. также</span><span class="sxs-lookup"><span data-stu-id="48909-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48909-133">**Создание приложения диспетчер устройств Windows Media**</span><span class="sxs-lookup"><span data-stu-id="48909-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




