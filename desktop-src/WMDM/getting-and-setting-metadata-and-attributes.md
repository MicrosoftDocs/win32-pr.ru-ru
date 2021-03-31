---
title: Получение и установка метаданных и атрибутов
description: Получение и установка метаданных и атрибутов
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Диспетчер устройств Windows Media, атрибуты
- Диспетчер устройств, атрибуты
- Классические приложения, атрибуты
- поставщики услуг, атрибуты
- инструкции по программированию, атрибуты
- attributes
- Диспетчер устройств Windows Media, метаданные
- Диспетчер устройств, метаданные
- Классические приложения, метаданные
- поставщики услуг, метаданные
- инструкции по программированию, метаданные
- метаданные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8697f62dac44f5aab4b08aa4f6c516ac35a17e4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888587"
---
# <a name="getting-and-setting-metadata-and-attributes"></a><span data-ttu-id="1f781-115">Получение и установка метаданных и атрибутов</span><span class="sxs-lookup"><span data-stu-id="1f781-115">Getting and Setting Metadata and Attributes</span></span>

<span data-ttu-id="1f781-116">Приложение может получить два вида информации о хранилище или устройстве: атрибуты и метаданные.</span><span class="sxs-lookup"><span data-stu-id="1f781-116">An application can get two kinds of information about a storage or device: attributes and metadata.</span></span> <span data-ttu-id="1f781-117">Атрибуты — это более простые логические значения, которые обычно описывают сведения о файловой системе, такие как наличие дочерних объектов в хранилище, возможность их переименования, чтения или удаления и т. д.</span><span class="sxs-lookup"><span data-stu-id="1f781-117">Attributes are simpler Boolean values that generally describe file system information, such as whether a storage has child objects, whether it can be renamed, read, or deleted, and so on.</span></span> <span data-ttu-id="1f781-118">Атрибуты извлекаются как значения флагов путем вызова [**ивмдмстораже:: InAttribute**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) или [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2).</span><span class="sxs-lookup"><span data-stu-id="1f781-118">Attributes are retrieved as flags values by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) or [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2).</span></span> <span data-ttu-id="1f781-119">Атрибуты задаются путем вызова [**IWMDMStorage3:: сетметадата**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span><span class="sxs-lookup"><span data-stu-id="1f781-119">Attributes are set by calling [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span>

<span data-ttu-id="1f781-120">Приложение также может запрашивать более сложные данные (числовые, строковые или другие типы данных) в качестве *метаданных*.</span><span class="sxs-lookup"><span data-stu-id="1f781-120">An application can also request more complex data (numeric, string, or other data types) as *metadata*.</span></span> <span data-ttu-id="1f781-121">Значения метаданных идентифицируются уникальными именами строк.</span><span class="sxs-lookup"><span data-stu-id="1f781-121">Metadata values are identified by unique string names.</span></span> <span data-ttu-id="1f781-122">Диспетчер устройств Windows Media определяет список строковых констант, которые можно использовать для запроса значений. Эти определенные значения перечислены в [константах метаданных](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1f781-122">Windows Media Device Manager defines a list of string constants that can be used to request values; these defined values are listed in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="1f781-123">Поставщик услуг может определять собственные константы, но вызывающее приложение должно учитывать эти определения, чтобы запрашивать или задавать значения пользовательских метаданных.</span><span class="sxs-lookup"><span data-stu-id="1f781-123">A service provider can define its own constants, but a calling application must be aware of these definitions in order to request or set these custom metadata values.</span></span> <span data-ttu-id="1f781-124">Приложение запрашивает метаданные с помощью вызова [**IWMDMStorage3::**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) IWMDMStorage4 или [**:: жетспеЦифиедметадата**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span><span class="sxs-lookup"><span data-stu-id="1f781-124">The application requests metadata by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span>

<span data-ttu-id="1f781-125">Важным аспектом получения и установки метаданных и атрибутов является понимание того, откуда берутся полученные значения.</span><span class="sxs-lookup"><span data-stu-id="1f781-125">An important aspect of getting and setting metadata and attributes is understanding where the retrieved values come from.</span></span> <span data-ttu-id="1f781-126">Поставщик услуг или устройство могут получать эти значения из различных мест, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="1f781-126">The service provider or the device can get these values from many different places, including the following:</span></span>

-   <span data-ttu-id="1f781-127">Из заголовка файла.</span><span class="sxs-lookup"><span data-stu-id="1f781-127">From the file header.</span></span> <span data-ttu-id="1f781-128">Например, в файле ASF скорость потока сохраняется в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="1f781-128">For example, in an ASF file, the bit rate is stored in the file header.</span></span>
-   <span data-ttu-id="1f781-129">Из значений, явно заданных приложением при вызове метода.</span><span class="sxs-lookup"><span data-stu-id="1f781-129">From values set explicitly by the application when calling a method.</span></span> <span data-ttu-id="1f781-130">Эти значения могут быть сохранены во внешнем хранилище метаданных в поставщике услуг или на устройстве.</span><span class="sxs-lookup"><span data-stu-id="1f781-130">These values may be saved in an external metadata store in the service provider or the device.</span></span> <span data-ttu-id="1f781-131">Это хранилище может не сохраняться, если устройство отключается или выключено.</span><span class="sxs-lookup"><span data-stu-id="1f781-131">This store may or may not persist when the device disconnects or turns off.</span></span> <span data-ttu-id="1f781-132">Например, количество воспроизводимых и пользовательских оценок обычно хранится во внешних хранилищах на компьютере или устройстве.</span><span class="sxs-lookup"><span data-stu-id="1f781-132">For example, the play count and user star ratings are typically stored in external stores on the computer or device.</span></span>
-   <span data-ttu-id="1f781-133">Изучив сведения, предоставленные файловой системой.</span><span class="sxs-lookup"><span data-stu-id="1f781-133">By examining information provided by the file system.</span></span> <span data-ttu-id="1f781-134">Например, доступен ли файл только для чтения или у папки есть дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="1f781-134">For example, whether a file is read-only or whether a folder has children.</span></span>
-   <span data-ttu-id="1f781-135">Путем открытия и анализа данных файла.</span><span class="sxs-lookup"><span data-stu-id="1f781-135">By opening and parsing the file data.</span></span>

<span data-ttu-id="1f781-136">Важно понимать, что свойство может храниться в нескольких местах (в заголовке файла и в локальном хранилище), а также может и не быть доступным для редактирования.</span><span class="sxs-lookup"><span data-stu-id="1f781-136">It is important to realize that a property might be stored in more than one location (within the file header and also in a local store), and that it may or may not be editable.</span></span> <span data-ttu-id="1f781-137">Например, изменение описания файла может быть постоянным или неустойчивым. Если поставщик услуг хранит описание локально, он не будет сохранен на устройстве.</span><span class="sxs-lookup"><span data-stu-id="1f781-137">For example, changing a file description may or may not be persistent; if the service provider stores the description locally, it will not persist on the device.</span></span> <span data-ttu-id="1f781-138">Аналогично, если в заголовке файла берется описание файла, изменение этого действия будет постоянным только в том случае, если поставщик услуг или устройство откроет и изменит данные заголовка.</span><span class="sxs-lookup"><span data-stu-id="1f781-138">Similarly, if the file description is taken from the file header, modifying this will only be persistent if the service provider or device opens and modifies the header data.</span></span> <span data-ttu-id="1f781-139">Большинство приложений наиболее эффективны, изменяя нужные значения, но не зависящие от свойств, которые должны быть постоянно изменены.</span><span class="sxs-lookup"><span data-stu-id="1f781-139">Most applications make a best attempt by changing desired values, but do not depend on any properties to be persistently changed.</span></span>

<span data-ttu-id="1f781-140">Дополнительные сведения о получении и установке значений приведены в соответствующих разделах, посвященных разработчикам приложений и разработчикам поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="1f781-140">More information on getting and setting values is given in the appropriate sections for application developers and service provider developers later in the documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f781-141">См. также</span><span class="sxs-lookup"><span data-stu-id="1f781-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f781-142">**Задачи, общие для приложений и поставщиков служб**</span><span class="sxs-lookup"><span data-stu-id="1f781-142">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




