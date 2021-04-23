---
title: Создание списка воспроизведения на устройстве
description: Создание списка воспроизведения на устройстве
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Диспетчер устройств Windows Media, списки воспроизведения
- Диспетчер устройств, списки воспроизведения
- рекомендации по программированию, списки воспроизведения
- Классические приложения, списки воспроизведения
- Создание приложений диспетчер устройств Windows Media, списков воспроизведения
- Абстрактные списки воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287cc406b795db07fde3f10103822dea32185a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329464"
---
# <a name="creating-a-playlist-on-the-device"></a><span data-ttu-id="5f115-109">Создание списка воспроизведения на устройстве</span><span class="sxs-lookup"><span data-stu-id="5f115-109">Creating a Playlist on the Device</span></span>

<span data-ttu-id="5f115-110">Пакет Windows Media диспетчер устройств SDK предоставляет средства для создания списка воспроизведения на устройстве с помощью приложения MTP.</span><span class="sxs-lookup"><span data-stu-id="5f115-110">The Windows Media Device Manager SDK provides the means for an MTP application to create a playlist on a device.</span></span> <span data-ttu-id="5f115-111">Этот тип списка воспроизведения называется *абстрактным* списком воспроизведения, так как файл, созданный на устройстве, не содержит данных мультимедиа, а только метаданные, которые содержат ссылки на файлы мультимедиа в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5f115-111">This type of playlist is called an *abstract* playlist, because the file created on the device contains no media data, but only metadata, which holds the links to media files in the playlist.</span></span>

<span data-ttu-id="5f115-112">Другие абстрактные элементы, которые можно создать на устройстве, включают альбомы (по сути, списки воспроизведения с дополнительными свойствами, такими как изображение обложки), контакты и сообщения.</span><span class="sxs-lookup"><span data-stu-id="5f115-112">Other abstract items that can be created on the device include albums (essentially playlists with extra properties such as cover art), contacts, and messages.</span></span>

<span data-ttu-id="5f115-113">**Создание списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="5f115-113">**To create a playlist**</span></span>

1.  <span data-ttu-id="5f115-114">Получите интерфейс [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) для целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="5f115-114">Acquire an [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) interface to the target device.</span></span>
2.  <span data-ttu-id="5f115-115">Вызовите [**IWMDMDevice3:: Property**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) , чтобы получить \_ свойство g всзвмдмформатссуппортед.</span><span class="sxs-lookup"><span data-stu-id="5f115-115">Call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to obtain the g\_wszWMDMFormatsSupported property.</span></span>
3.  <span data-ttu-id="5f115-116">Если форматы списка воспроизведения не поддерживаются, запретите отправку списков воспроизведения на устройство и пропустите следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="5f115-116">If no playlist formats are supported, disallow sending playlists to the device, and skip the following steps.</span></span> <span data-ttu-id="5f115-117">В противном случае выберите код формата, поддерживаемый устройством, который соответствует наиболее близкому типу объекта.</span><span class="sxs-lookup"><span data-stu-id="5f115-117">Otherwise, choose the device-supported format code that matches most closely the intended object type.</span></span> <span data-ttu-id="5f115-118">\_ \_ \_ Наиболее часто поддерживаются коды формата универсальных вмдм ФОРМАТКОДЕ абстрактаудиовидеоплайлист и вмдм форматкоде \_ абстрактаудиолайлист.</span><span class="sxs-lookup"><span data-stu-id="5f115-118">The generic WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST and WMDM\_FORMATCODE\_ABSTRACTAUDIOLAYLIST format codes are the most commonly supported.</span></span>
4.  <span data-ttu-id="5f115-119">Получите интерфейс [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) для хранилища (корневой каталог или папку), в котором нужно создать объект.</span><span class="sxs-lookup"><span data-stu-id="5f115-119">Obtain an [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) interface for the storage (the root or a folder) where you want to create the object.</span></span> <span data-ttu-id="5f115-120">Некоторые устройства работают лучше, если объект списка воспроизведения размещается в папке верхнего уровня с именем "списки воспроизведения".</span><span class="sxs-lookup"><span data-stu-id="5f115-120">Some devices work best if the playlist object is placed in a top level folder named "Playlists".</span></span>
5.  <span data-ttu-id="5f115-121">Создайте пустой объект метаданных с помощью [**IWMDMStorage3:: креатимптиметадатаобжект**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span><span class="sxs-lookup"><span data-stu-id="5f115-121">Create an empty metadata object by using [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span></span>
6.  <span data-ttu-id="5f115-122">Используя интерфейс **ивмдмметадата** , полученный на предыдущем шаге, вызовите [**Ивмдмметадата:: AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) , чтобы добавить выбранный код формата (из шага 3) в свойства метаданных хранилища.</span><span class="sxs-lookup"><span data-stu-id="5f115-122">Using the **IWMDMMetaData** interface obtained in the previous step, call [**IWMDMMetaData::AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) to add your chosen format code (from step 3) to the storage metadata properties.</span></span>
7.  <span data-ttu-id="5f115-123">Получите интерфейс [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) из интерфейса **IWMDMStorage3** .</span><span class="sxs-lookup"><span data-stu-id="5f115-123">Obtain the [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) interface from the **IWMDMStorage3** interface.</span></span>
8.  <span data-ttu-id="5f115-124">Вызовите [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) , чтобы вставить новый файл списка воспроизведения в выбранное хранилище.</span><span class="sxs-lookup"><span data-stu-id="5f115-124">Call [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to insert a new playlist file in the selected storage.</span></span> <span data-ttu-id="5f115-125">Этот файл содержит метаданные, представленные интерфейсом **ивмдмметадата** , созданным на шаге 5 и передаваемым в **Insert3**.</span><span class="sxs-lookup"><span data-stu-id="5f115-125">This file contains the metadata represented by the **IWMDMMetaData** interface you created in step 5 and passed to **Insert3**.</span></span> <span data-ttu-id="5f115-126">Метод возвращает интерфейс **ивмдмстораже** для файла списка воспроизведения. Вы можете запросить интерфейс [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) .</span><span class="sxs-lookup"><span data-stu-id="5f115-126">The method returns an **IWMDMStorage** interface for the playlist file; you can query for the [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) interface.</span></span>
9.  <span data-ttu-id="5f115-127">Вызовите [**IWMDMStorage4:: сетреференцес**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) , чтобы создать ссылки на интерфейсы **ивмдмстораже** файлов мультимедиа в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5f115-127">Call [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) to create references to the **IWMDMStorage** interfaces of the media files in the playlist.</span></span>

<span data-ttu-id="5f115-128">Пример кода см. в описании \_ функции онкреатеплайлист в [примере классического приложения](sample-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="5f115-128">For example code, see the \_OnCreatePlaylist function in the [Sample Desktop Application](sample-desktop-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="5f115-129">Поставщик услуг MTP, предоставляемый корпорацией Майкрософт, позволяет приложению задавать ссылки в метаданных.</span><span class="sxs-lookup"><span data-stu-id="5f115-129">The Microsoft-provided MTP service provider enables an application to set references in metadata.</span></span> <span data-ttu-id="5f115-130">Чтобы реализовать списки воспроизведения, приложение должно взаимодействовать с устройством MTP или использовать пользовательский поставщик услуг, который может обрабатывать абстрактные объекты.</span><span class="sxs-lookup"><span data-stu-id="5f115-130">To implement playlists, your application must be communicating with an MTP device or using a custom service provider that can handle abstract objects.</span></span> <span data-ttu-id="5f115-131">Поставщик служб CE обрабатывает списки воспроизведения и объекты альбома.</span><span class="sxs-lookup"><span data-stu-id="5f115-131">The CE service provider handles playlist and album objects.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5f115-132">См. также</span><span class="sxs-lookup"><span data-stu-id="5f115-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f115-133">**Запись файлов на устройство**</span><span class="sxs-lookup"><span data-stu-id="5f115-133">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




