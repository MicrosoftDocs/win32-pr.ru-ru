---
title: Изучение устройства
description: Изучение устройства
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Диспетчер устройств Windows Media, изучение устройств
- Диспетчер устройств, изучение устройств
- Программное руководством, изучение устройств
- Классические приложения, изучение устройств
- Создание приложений диспетчер устройств Windows Media, изучение устройств
- изучение устройств
- хранилищах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc154960a4c95efbdf2626271ba90000df99ae8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410989"
---
# <a name="exploring-a-device"></a><span data-ttu-id="67994-110">Изучение устройства</span><span class="sxs-lookup"><span data-stu-id="67994-110">Exploring a Device</span></span>

<span data-ttu-id="67994-111">Изучение устройства похоже на изучение диска.</span><span class="sxs-lookup"><span data-stu-id="67994-111">Exploring a device is similar to exploring a disk drive.</span></span> <span data-ttu-id="67994-112">Все объекты на устройстве называются *хранилищами*.</span><span class="sxs-lookup"><span data-stu-id="67994-112">All objects on a device are called *storages*.</span></span> <span data-ttu-id="67994-113">Хранилищем может быть файл, папка или абстрактный объект (например, список воспроизведения) на устройстве.</span><span class="sxs-lookup"><span data-stu-id="67994-113">A storage can be a file, folder, or abstract object (such as a playlist) on the device.</span></span> <span data-ttu-id="67994-114">Необходимо изучить атрибуты и метаданные хранилища (если они поддерживаются), чтобы понять, какой тип хранилища он имеет.</span><span class="sxs-lookup"><span data-stu-id="67994-114">You must examine a storage's attributes and metadata (if supported) to understand what kind of storage it is.</span></span> <span data-ttu-id="67994-115">Хранилища организованы иерархически на устройстве; Каждое хранилище имеет ровно один родительский объект, и все хранилища в конечном итоге попадут в одно хранилище корневых устройств, обычно именуемое " \\ ".</span><span class="sxs-lookup"><span data-stu-id="67994-115">Storages are organized hierarchically on the device; every storage has exactly one parent, and all storages ultimately descend from a single root device storage, typically named "\\".</span></span>

<span data-ttu-id="67994-116">Следующие шаги описывают изучение устройства:</span><span class="sxs-lookup"><span data-stu-id="67994-116">The following steps describe how to explore a device:</span></span>

1.  <span data-ttu-id="67994-117">Получите интерфейс [**ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) устройства, как описано в разделе [Перечисление устройств](enumerating-devices.md).</span><span class="sxs-lookup"><span data-stu-id="67994-117">Get the [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface of a device as described in [Enumerating Devices](enumerating-devices.md).</span></span>
2.  <span data-ttu-id="67994-118">Вызовите метод [**ивмдмдевице:: енумстораже**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) , чтобы получить интерфейс [**ивмдменумстораже**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) .</span><span class="sxs-lookup"><span data-stu-id="67994-118">Call [**IWMDMDevice::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) to retrieve an [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) interface.</span></span> <span data-ttu-id="67994-119">Этот интерфейс используется для получения всех дочерних объектов хранилища, возвращающих этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="67994-119">This interface is used to get all child objects of the storage that returns this interface.</span></span> <span data-ttu-id="67994-120">При получении этого интерфейса с устройства, как мы здесь, он будет хранить только одно хранилище: хранилище корневого устройства.</span><span class="sxs-lookup"><span data-stu-id="67994-120">When getting this interface from the device, as we are here, it will hold only one storage: the root device storage.</span></span>
3.  <span data-ttu-id="67994-121">Вызовите метод [**ивмдменумстораже:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) со значением счетчика 1, чтобы получить интерфейс [**ивмдмстораже**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) для хранилища корневого устройства.</span><span class="sxs-lookup"><span data-stu-id="67994-121">Call [**IWMDMEnumStorage::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) with a count of 1 to retrieve the [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) interface for the root device storage.</span></span> <span data-ttu-id="67994-122">(На устройстве нельзя запрашивать более одного дочернего элемента.)</span><span class="sxs-lookup"><span data-stu-id="67994-122">(You cannot request more than one child from the device.)</span></span>
4.  <span data-ttu-id="67994-123">Проверьте все хранилища на устройстве, рекурсивно вызвав [**ивмдмстораже:: енумстораже**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) , а затем **Ивмдменумстораже:: Next** , чтобы получить дочерние элементы хранилища.</span><span class="sxs-lookup"><span data-stu-id="67994-123">Examine all storages on the device by recursively calling [**IWMDMStorage::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) and then **IWMDMEnumStorage::Next** to get children of a storage.</span></span> <span data-ttu-id="67994-124">Чтобы узнать, есть ли у хранилища дочерние элементы, чтобы избежать вызовов **енумстораже** и **Next**, можно вызвать [**ивмдмстораже:: OutAttribute**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) , чтобы проверить наличие флагов вмдма \_ attr, \_ \_ имеющих файлы или вмдм в атрибуте \_ \_ Storage \_ attr \_ есть \_ папки.</span><span class="sxs-lookup"><span data-stu-id="67994-124">To see if a storage has children to avoid the calls to **EnumStorage** and **Next**, you can call [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) to check for the flags WMDM\_STORAGE\_ATTR\_HAS\_FILES or WMDM\_STORAGE\_ATTR\_HAS\_FOLDERS.</span></span> <span data-ttu-id="67994-125">Дополнительные сведения о том, как получить свойства хранилища, см. в статьях [Получение и установка метаданных и атрибутов](getting-and-setting-metadata-and-attributes.md) , а также [Получение и установка метаданных и атрибутов в приложении](getting-and-setting-metadata-and-attributes-in-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="67994-125">For more information about how to get the properties of a storage, see [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md) and [Getting and Setting Metadata and Attributes in the Application](getting-and-setting-metadata-and-attributes-in-the-application.md).</span></span>

<span data-ttu-id="67994-126">Диспетчер устройств Windows Media не предоставляет стандартный набор папок для хранения мультимедиа определенного типа (например, папка "Мои списки воспроизведения" для списков воспроизведения).</span><span class="sxs-lookup"><span data-stu-id="67994-126">Windows Media Device Manager does not expose a standard set of folders to hold media of a specific type (for example, a "My Playlists" folder for playlists).</span></span> <span data-ttu-id="67994-127">Каждое устройство имеет уникальную файловую систему, и вам придется выбрать подходящее место для поиска или отправки определенного файла.</span><span class="sxs-lookup"><span data-stu-id="67994-127">Every device has a unique file system, and you will have to decide on an appropriate place to look for, or to send, a specific file.</span></span>

> [!Note]  
> <span data-ttu-id="67994-128">Проводник Windows может отображать виртуальные папки, которые на самом деле не существуют на устройстве.</span><span class="sxs-lookup"><span data-stu-id="67994-128">Windows Explorer can show virtual folders that do not actually exist on the device.</span></span> <span data-ttu-id="67994-129">Например, виртуальные папки — это папки "Media" и "Data", отображаемые для устройств MTP.</span><span class="sxs-lookup"><span data-stu-id="67994-129">Example virtual folders are the "Media" and "Data" folders displayed for MTP devices.</span></span> <span data-ttu-id="67994-130">Эти папки создаются Windows, чтобы упростить загрузку для конечных пользователей. они на самом деле не существуют на устройстве.</span><span class="sxs-lookup"><span data-stu-id="67994-130">These folders are created by Windows to make downloads simpler for end users; they do not actually exist on the device.</span></span> <span data-ttu-id="67994-131">Приложение не должно зависеть от поиска этих типов общих папок.</span><span class="sxs-lookup"><span data-stu-id="67994-131">Your application should not depend on finding these types of general folders.</span></span> <span data-ttu-id="67994-132">И наоборот, проводник Windows может не показывать некоторые папки или объекты, существующие на устройстве (например, списки воспроизведения).</span><span class="sxs-lookup"><span data-stu-id="67994-132">Conversely, Windows Explorer might not show some folders or objects that do exist on the device (for example, playlists).</span></span>

 

<span data-ttu-id="67994-133">В следующем примере кода C++ показано рекурсивное исследование устройства.</span><span class="sxs-lookup"><span data-stu-id="67994-133">The following C++ example code demonstrates the recursive exploration of a device.</span></span> <span data-ttu-id="67994-134">В нем используются две функции:</span><span class="sxs-lookup"><span data-stu-id="67994-134">It uses two functions:</span></span>

-   <span data-ttu-id="67994-135">Експлоредевице — начальная функция, которая получает указатель устройства и получает указатель на корневой перечислитель для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="67994-135">ExploreDevice, a starting function that receives a device pointer and obtains a pointer to the root enumerator for that device.</span></span>
-   <span data-ttu-id="67994-136">Рекурсивиксплорестораже, который вызывается для рекурсивного изучения устройства.</span><span class="sxs-lookup"><span data-stu-id="67994-136">RecursiveExploreStorage, which is called to explore a device recursively.</span></span>


```C++
// Get the root enumerator and start the recursive function.
HRESULT ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    if (SUCCEEDED(hr))
    {
        RecursiveExploreStorage(pEnumStorage);
    }
    return hr;
}

// Recursively explore a storage.
void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;

    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    while((pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK) && (numRetrieved == 1))
    {
        // Get the name of the object.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the retrieved storage name

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            if (SUCCEEDED(hr)
            {
                RecursiveExploreStorage(pEnumSubStorage);
            }
        }
        pStorage.Release();
    } // Get the next storage pointer.
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="67994-137">См. также</span><span class="sxs-lookup"><span data-stu-id="67994-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67994-138">**Создание приложения диспетчер устройств Windows Media**</span><span class="sxs-lookup"><span data-stu-id="67994-138">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




