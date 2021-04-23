---
description: Объектная модель VDS
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: Объектная модель VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104273166"
---
# <a name="vds-object-model"></a><span data-ttu-id="7b286-103">Объектная модель VDS</span><span class="sxs-lookup"><span data-stu-id="7b286-103">VDS Object Model</span></span>

<span data-ttu-id="7b286-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7b286-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="7b286-105">Служба VDS обеспечивает косвенный доступ к устройствам хранения на основе узлов, таким как диски и устройства чтения компакт-дисков, а также к массивам дисков, управляемым аппаратными RAID-контроллерами.</span><span class="sxs-lookup"><span data-stu-id="7b286-105">VDS provides indirect access to host-based storage devices, such as disks and CD-ROM devices, and to disk arrays that are managed by hardware RAID controllers.</span></span> <span data-ttu-id="7b286-106">Хотя некоторые сущности хранилища моделируют физические устройства, другие виртуальные конструкции модели: тома, секции и т. д.</span><span class="sxs-lookup"><span data-stu-id="7b286-106">While some storage entities model physical devices, others model virtual constructs: volumes, partitions, and so on.</span></span> <span data-ttu-id="7b286-107">Объекты, описанные в этом разделе, представляют как физические, так и виртуальные сущности службы VDS.</span><span class="sxs-lookup"><span data-stu-id="7b286-107">The objects that are described in this topic represent both the physical and virtual entities of VDS.</span></span>

<span data-ttu-id="7b286-108">Приложения вызывают методы, предоставляемые этими объектами, и служба VDS вызывает соответствующий поставщик для выполнения запрошенных операций с хранилищем.</span><span class="sxs-lookup"><span data-stu-id="7b286-108">Applications call the methods that are exposed by these objects and VDS calls the appropriate provider to perform the requested storage operations.</span></span> <span data-ttu-id="7b286-109">Приложение никогда не вызывает программу поставщика напрямую.</span><span class="sxs-lookup"><span data-stu-id="7b286-109">An application never calls a provider program directly.</span></span>

### <a name="classification-of-objects"></a><span data-ttu-id="7b286-110">Классификация объектов</span><span class="sxs-lookup"><span data-stu-id="7b286-110">Classification of Objects</span></span>

<span data-ttu-id="7b286-111">Как показано на следующем рисунке, программы поставщика программного обеспечения реализуют объекты, которые моделируют сущности на основе узла. программы поставщиков оборудования реализуют объекты, которые моделируют внутренние и внешние аппаратные RAID-устройства; остальные общие объекты не зависят от поставщика или реализуются службой VDS.</span><span class="sxs-lookup"><span data-stu-id="7b286-111">As the following illustration shows, software provider programs implement objects that model host-based entities; hardware provider programs implement objects that model internal and external hardware RAID devices; the remaining common objects are either provider-independent, or are implemented by VDS.</span></span> <span data-ttu-id="7b286-112">Диск, который не является объектом VDS, является термином для универсального носителя хранилища, который состоит из экстентов диска или диска.</span><span class="sxs-lookup"><span data-stu-id="7b286-112">A spindle, which is not a VDS object, is a term for generic storage media that comprises of disk or drive extents.</span></span>

![Схема, на которой показана классификация объектов, определенных как "общие объекты", "объекты поставщика программного обеспечения" и "объекты поставщика оборудования".](images/vdsobjectmodel.png)

<span data-ttu-id="7b286-114">Дополнительные сведения о поведении каждого объекта см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="7b286-114">To learn more about the behavior of each object, select from the following topics:</span></span>

-   <span data-ttu-id="7b286-115">Загрузчике служб и объекты службы см. в разделе [объекты запуска и службы](startup-and-service-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7b286-115">Service loader and service objects, see [Startup and Service Objects](startup-and-service-objects.md).</span></span>
-   <span data-ttu-id="7b286-116">Перечисления и асинхронных объектов см. в разделе [вспомогательные объекты](helper-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7b286-116">Enumeration and async objects, see [Helper Objects](helper-objects.md).</span></span>
-   <span data-ttu-id="7b286-117">Объект поставщика см. в разделе [объект поставщика](provider-object.md).</span><span class="sxs-lookup"><span data-stu-id="7b286-117">Provider object, see [Provider Object](provider-object.md).</span></span>
-   <span data-ttu-id="7b286-118">Объекты "Pack", "диск", "том" и "Плекс" см. в разделе [объекты поставщика программного обеспечения](software-provider-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7b286-118">Pack, disk, volume, and volume plex objects, see [Software Provider Objects](software-provider-objects.md).</span></span>
-   <span data-ttu-id="7b286-119">Подсистема, контроллер, диск, LUN и объекты плекса LUN см. в разделе [объекты поставщика оборудования](hardware-provider-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7b286-119">Subsystem, controller, drive, LUN, and LUN plex objects, see [Hardware Provider Objects](hardware-provider-objects.md).</span></span>

### <a name="object-creation"></a><span data-ttu-id="7b286-120">Создание объектов</span><span class="sxs-lookup"><span data-stu-id="7b286-120">Object Creation</span></span>

<span data-ttu-id="7b286-121">Выполнение операций конфигурации и запросов, связанных с созданием объектов, может занять значительное время; Таким образом, служба VDS вызывает все методы асинхронно.</span><span class="sxs-lookup"><span data-stu-id="7b286-121">The configuration and query operations that are associated with object creation can take considerable time to complete; as such, VDS invokes all methods asynchronously.</span></span> <span data-ttu-id="7b286-122">Поставщик обнаружения возвращает все события завершения, ошибки или изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="7b286-122">The discovering provider returns all completion, error, or state change events.</span></span> <span data-ttu-id="7b286-123">Поставщики программного обеспечения также заносить в журнал все ошибки и значительные изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="7b286-123">Software providers also log all the errors and significant state changes.</span></span>

### <a name="object-deletion"></a><span data-ttu-id="7b286-124">Удаление объекта</span><span class="sxs-lookup"><span data-stu-id="7b286-124">Object Deletion</span></span>

<span data-ttu-id="7b286-125">Несколько методов VDS удаляют или преобразуют объекты VDS.</span><span class="sxs-lookup"><span data-stu-id="7b286-125">Several VDS methods delete or transform VDS objects.</span></span> <span data-ttu-id="7b286-126">Вызывающий объект может хранить ссылку, используя указатель интерфейса, удаленному объекту после возврата метода.</span><span class="sxs-lookup"><span data-stu-id="7b286-126">A caller can hold a reference, by way of an interface pointer, to a deleted object after the method returns.</span></span> <span data-ttu-id="7b286-127">Когда вызывающий объект освобождает интерфейс, служба VDS удаляет объект.</span><span class="sxs-lookup"><span data-stu-id="7b286-127">When the caller releases the interface, VDS deletes the object.</span></span>

<span data-ttu-id="7b286-128">В отношении удаления объектов вызывающие объекты должны отменять вызов любого объекта, кроме метода [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="7b286-128">With regard to object deletion, callers should refrain from invoking anything except the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on these interfaces.</span></span> <span data-ttu-id="7b286-129">Поставщик должен быть достаточно надежным для работы с вызывающими объектами аномального. Если вызывающий объект вызывает метод для удаленного объекта, поставщик должен вернуть **объект VDS E в \_ \_ \_ удаленном** виде.</span><span class="sxs-lookup"><span data-stu-id="7b286-129">The provider must be robust enough to deal with errant callers; if a caller invokes a method on a deleted object, the provider should return **VDS\_E\_OBJECT\_DELETED**.</span></span>

### <a name="service-initialization"></a><span data-ttu-id="7b286-130">Инициализация службы</span><span class="sxs-lookup"><span data-stu-id="7b286-130">Service Initialization</span></span>

<span data-ttu-id="7b286-131">Служба VDS предоставляет идентификатор класса (CLSID) для загрузчика службы и объектов службы, но только CLSID загрузчика службы является общедоступным.</span><span class="sxs-lookup"><span data-stu-id="7b286-131">VDS supplies a class identifier (Clsid) for the service loader and the service objects, but only the service loader Clsid is public.</span></span> <span data-ttu-id="7b286-132">Инициализация службы происходит, когда поставщики, вызывающее приложение и служба выполняют следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="7b286-132">Service initialization occurs when the providers, a calling application, and the service perform the following tasks:</span></span>

-   <span data-ttu-id="7b286-133">Каждый новый поставщик вызывает метод [**ивдсадмин:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) во время установки для регистрации в службе VDS.</span><span class="sxs-lookup"><span data-stu-id="7b286-133">Each new provider invokes the [**IVdsAdmin::RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) method during installation to register with VDS.</span></span> <span data-ttu-id="7b286-134">Вызов создает раздел реестра в СИСТЕМном кусте, определяемый идентификатором GUID объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="7b286-134">The call creates a registry key under the SYSTEM hive, identified by the object GUID of the provider.</span></span> <span data-ttu-id="7b286-135">В этом разделе содержится идентификатор CLSID объекта поставщика, имя, версия и идентификатор GUID версии поставщика.</span><span class="sxs-lookup"><span data-stu-id="7b286-135">Contained under this key is the Clsid of the provider object, the name, version, and the version GUID of the provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="7b286-136">Идентификаторы GUID объектов поставщика являются постоянными; идентификаторы GUID объектов программного и аппаратного обеспечения не являются.</span><span class="sxs-lookup"><span data-stu-id="7b286-136">Provider object GUIDs are persistent; software and hardware object GUIDs are not.</span></span>

     

-   <span data-ttu-id="7b286-137">Приложение вызывает функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , передавая CLSID загрузчика службы в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="7b286-137">An application calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, passing the service loader Clsid as an argument.</span></span> <span data-ttu-id="7b286-138">Используя указатель на объект загрузчика службы, приложение может запустить службу VDS локально или удаленно, передав имя нужного компьютера в качестве параметра в метод [**ивдссервицелоадер:: лоадсервице**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) .</span><span class="sxs-lookup"><span data-stu-id="7b286-138">With a pointer to the service loader object, the application can start VDS either locally or remotely by passing the desired computer name as a parameter to the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method.</span></span>
-   <span data-ttu-id="7b286-139">При присоединении к службе первого приложения служба VDS сначала вызывает [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для каждого идентификатора CLSID, найденного в разделе реестра, а затем вызывает метод [**ивдспровидерпривате:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) для каждого поставщика, чтобы инициализировать программы.</span><span class="sxs-lookup"><span data-stu-id="7b286-139">When the initial application attaches to the service, VDS first calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on each Clsid found under the registry key, and then calls the [**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) method on each provider to initialize the programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b286-140">См. также</span><span class="sxs-lookup"><span data-stu-id="7b286-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b286-141">О службе VDS</span><span class="sxs-lookup"><span data-stu-id="7b286-141">About VDS</span></span>](about-vds.md)
</dt> <dt>

[<span data-ttu-id="7b286-142">**Ивдсадмин:: RegisterProvider**</span><span class="sxs-lookup"><span data-stu-id="7b286-142">**IVdsAdmin::RegisterProvider**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[<span data-ttu-id="7b286-143">**Ивдссервицелоадер:: Лоадсервице**</span><span class="sxs-lookup"><span data-stu-id="7b286-143">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="7b286-144">**Ивдспровидерпривате:: OnLoad**</span><span class="sxs-lookup"><span data-stu-id="7b286-144">**IVdsProviderPrivate::OnLoad**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
