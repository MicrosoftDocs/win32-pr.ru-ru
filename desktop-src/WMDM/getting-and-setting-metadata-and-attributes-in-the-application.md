---
title: Доступ к метаданным и атрибутам в приложении
description: Получение и установка метаданных и атрибутов в приложении
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Диспетчер устройств Windows Media, метаданные
- Диспетчер устройств, метаданные
- инструкции по программированию, метаданные
- Классические приложения, метаданные
- Создание приложений диспетчер устройств Windows Media, метаданные
- метаданные
- Диспетчер устройств Windows Media, атрибуты
- Диспетчер устройств, атрибуты
- инструкции по программированию, атрибуты
- Классические приложения, атрибуты
- Создание приложений диспетчер устройств Windows Media, атрибуты
- attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/27/2019
ms.locfileid: "104335763"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a><span data-ttu-id="2c791-115">Доступ к метаданным и атрибутам в приложении</span><span class="sxs-lookup"><span data-stu-id="2c791-115">Accessing metadata and attributes in the app</span></span>

<span data-ttu-id="2c791-116">Общие сведения о метаданных и атрибутах доступны в статье [Получение и установка метаданных и атрибутов](getting-and-setting-metadata-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="2c791-116">A general discussion of metadata and attributes is available in [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md).</span></span> <span data-ttu-id="2c791-117">В этом разделе рассматриваются определенные вызовы методов приложений для получения или задания значений.</span><span class="sxs-lookup"><span data-stu-id="2c791-117">This section covers specific application method calls to retrieve or set values.</span></span>

<span data-ttu-id="2c791-118">Приложения могут извлекать атрибуты или метаданные о конкретном хранилище путем вызова [**ивмдмстораже:: InAttribute**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3::-Metadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) или [**IWMDMStorage4:: жетспеЦифиедметадата**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span><span class="sxs-lookup"><span data-stu-id="2c791-118">Applications can retrieve attributes or metadata about a specific storage by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span> <span data-ttu-id="2c791-119">Параметр- **Metadata** извлекает полную коллекцию всех метаданных, связанных с хранилищем, и приложение может перечислить все значения или запросить определенные значения из коллекции.</span><span class="sxs-lookup"><span data-stu-id="2c791-119">**GetMetadata** retrieves a full collection of all the metadata associated with a storage, and the application can then enumerate through all values or request specific values from the collection.</span></span> <span data-ttu-id="2c791-120">**ЖетспеЦифиедметадата** создает объект метаданных от имени вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="2c791-120">**GetSpecifiedMetadata** creates a metadata object on behalf of the caller.</span></span> <span data-ttu-id="2c791-121">Вызывающий объект может запросить подмножество доступных данных, заполнив параметр *ппвсзпропнамес* массивом требуемых строк свойств Windows Media Диспетчер устройств и количеством этого массива.</span><span class="sxs-lookup"><span data-stu-id="2c791-121">The caller may request a subset of the available data by filling in the *ppwszPropNames* parameter with an array of the desired Windows Media Device Manager property strings, and the count of that array.</span></span> <span data-ttu-id="2c791-122">Возвращенный объект метаданных будет заполнен этими свойствами, которые можно получить.</span><span class="sxs-lookup"><span data-stu-id="2c791-122">The returned metadata object will be filled with those properties that could be retrieved.</span></span> <span data-ttu-id="2c791-123">Эти свойства, которые не удалось получить, будут отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="2c791-123">Those properties that couldn't be retrieved will be absent.</span></span> <span data-ttu-id="2c791-124">Метаданные возвращаются на основе наилучшей силы.</span><span class="sxs-lookup"><span data-stu-id="2c791-124">Metadata is returned on a best-effort basis.</span></span>

<span data-ttu-id="2c791-125">Устройство может устанавливать атрибуты или метаданные в хранилище путем вызова [**ивмдмстораже:: сетаттрибутес**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)или [**IWMDMStorage3:: сетметадата**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span><span class="sxs-lookup"><span data-stu-id="2c791-125">A device can set attributes or metadata on a storage by calling [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2::SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2), or [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span> <span data-ttu-id="2c791-126">Обратите внимание, что не существует гарантии, что все значения будут сохранены, так как они могут храниться в непостоянном внешнем хранилище файлов, они могут не поддерживаться или устройство может не поддерживать доступ к свойствам в качестве записываемых.</span><span class="sxs-lookup"><span data-stu-id="2c791-126">Note that there is no guarantee that any values set will persist, because they may be stored in a non-persistent external file store, the values may not be supported, or, the device may not support the properties as writeable.</span></span>

<span data-ttu-id="2c791-127">Также можно получить или задать метаданные о устройстве, вызвав [**IWMDMDevice3::-Property**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) или [**IWMDMDevice3:: SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty).</span><span class="sxs-lookup"><span data-stu-id="2c791-127">You can also get or set metadata about a device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) or [**IWMDMDevice3::SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty).</span></span> <span data-ttu-id="2c791-128">Существует отдельная таблица констант метаданных устройства, перечисленных в конце [констант метаданных](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2c791-128">There is a separate table of device metadata constants listed at the end of [Metadata Constants](metadata-constants.md).</span></span>

<span data-ttu-id="2c791-129">Примеры использования этих методов приведены в справочной документации по каждому методу.</span><span class="sxs-lookup"><span data-stu-id="2c791-129">Examples of using these methods are given in each method's reference documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c791-130">См. также</span><span class="sxs-lookup"><span data-stu-id="2c791-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c791-131">**Создание приложения диспетчер устройств Windows Media**</span><span class="sxs-lookup"><span data-stu-id="2c791-131">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="2c791-132">**Получение и установка метаданных и атрибутов**</span><span class="sxs-lookup"><span data-stu-id="2c791-132">**Getting and Setting Metadata and Attributes**</span></span>](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




