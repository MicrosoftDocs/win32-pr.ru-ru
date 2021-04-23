---
title: Включение PnP для устройств
description: Включение PnP для устройств
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Диспетчер устройств Windows Media, устройства PnP
- Диспетчер устройств, устройства PnP
- Программное обеспеченное программирование, устройства PnP
- поставщики услуг, устройства PnP
- Создание поставщиков услуг, устройств PnP
- Устройства PnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888127"
---
# <a name="enabling-pnp-for-devices"></a><span data-ttu-id="e70b8-109">Включение PnP для устройств</span><span class="sxs-lookup"><span data-stu-id="e70b8-109">Enabling PnP for Devices</span></span>

<span data-ttu-id="e70b8-110">Windows Media диспетчер устройств отслеживает уведомления о получении и удалении устройств, которые объявляют интерфейс мобильного устройства воспроизведения аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="e70b8-110">Windows Media Device Manager monitors arrival and removal notifications of devices that advertise a Portable Audio Player device interface.</span></span> <span data-ttu-id="e70b8-111">При поступлении такого устройства Windows Media диспетчер устройств запрашивает параметр устройства с именем *вмдмспклсид* для идентификатора класса поставщика услуг, ответственного за это устройство.</span><span class="sxs-lookup"><span data-stu-id="e70b8-111">On the arrival of such a device, Windows Media Device Manager queries a device parameter named *WMDMSPCLSID* for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="e70b8-112">Windows Media диспетчер устройств вызывает [**IMDServiceProvider2:: креатедевице**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) для этого поставщика услуг, чтобы создать объект устройства, который предоставляется приложению как объект [**ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="e70b8-112">Windows Media Device Manager calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on this service provider to create a device object, which is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

<span data-ttu-id="e70b8-113">Поставщик услуг может либо работать с устройствами PnP, либо устройствами, не поддерживающими PnP. Он не может работать с обоими типами.</span><span class="sxs-lookup"><span data-stu-id="e70b8-113">A service provider can either handle PnP devices, or non-PnP devices; it cannot handle both types.</span></span>

<span data-ttu-id="e70b8-114">Чтобы устройство работало с предыдущим механизмом (и таким образом включить уведомления о получении и удалении устройства в Windows Media диспетчер устройств Applications), должны выполняться следующие требования.</span><span class="sxs-lookup"><span data-stu-id="e70b8-114">For a device to work with the preceding mechanism (and thus enable arrival and removal notifications for the device under Windows Media Device Manager applications), the following requirements must be met:</span></span>

-   <span data-ttu-id="e70b8-115">Драйвер устройства этого устройства должен объявлять интерфейс устройства Windows Media диспетчер устройств Portable Audio Player.</span><span class="sxs-lookup"><span data-stu-id="e70b8-115">The device driver of this device must advertise the Windows Media Device Manager Portable Audio Player device interface.</span></span> <span data-ttu-id="e70b8-116">GUID для этого интерфейса устройства определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e70b8-116">The GUID for this device interface is defined as:</span></span>

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > <span data-ttu-id="e70b8-117">Устройство не должно объявлять этот интерфейс, если устройство объявляет интерфейс тома (определенный как Волумеклассгуид или GUID \_ девинтерфаце \_ в виниоктл. h).</span><span class="sxs-lookup"><span data-stu-id="e70b8-117">A device should not advertise this interface if the device advertises the Volume interface (defined as VolumeClassGuid or GUID\_DEVINTERFACE\_VOLUME in winioctl.h).</span></span> <span data-ttu-id="e70b8-118">Если устройство объявляет интерфейс тома, оно уже включено с поддержкой PnP в Windows Media диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="e70b8-118">If the device advertises the Volume Interface, it is already PnP-enabled under Windows Media Device Manager.</span></span>

     

    <span data-ttu-id="e70b8-119">-И/ИЛИ-</span><span class="sxs-lookup"><span data-stu-id="e70b8-119">-AND/OR-</span></span>

    <span data-ttu-id="e70b8-120">Новый подраздел реестра для поставщика услуг должен быть создан внутри подраздела HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows Media Диспетчер устройств \\ кновндевицес.</span><span class="sxs-lookup"><span data-stu-id="e70b8-120">A new registry subkey for the service provider must be created inside the subkey HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\KnownDevices.</span></span> <span data-ttu-id="e70b8-121">У этого ключа должно быть имя поставщика услуг, и в нем должны быть следующие две \_ записи реестра SZ:</span><span class="sxs-lookup"><span data-stu-id="e70b8-121">This key should have the name of your service provider and must have the following two Reg\_SZ value entries:</span></span>

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   <span data-ttu-id="e70b8-122">Устройство должно иметь параметр устройства с именем ВМДМСПКЛСИД.</span><span class="sxs-lookup"><span data-stu-id="e70b8-122">The device must have a device parameter named WMDMSPCLSID.</span></span> <span data-ttu-id="e70b8-123">Значение этого параметра должно быть задано в качестве идентификатора CLSID поставщика службы в форме строки.</span><span class="sxs-lookup"><span data-stu-id="e70b8-123">The value of this parameter should be set as the CLSID of the service provider in a string form.</span></span> <span data-ttu-id="e70b8-124">Дополнительные сведения о параметрах устройств см. в разделе [Параметры устройства](device-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e70b8-124">For more information about device parameters, see [Device Parameters](device-parameters.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="e70b8-125">Значение параметра должно быть идентификатором CLSID, а не ProgID поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e70b8-125">The parameter value must be the CLSID, not the ProgID of the service provider.</span></span>

     

-   <span data-ttu-id="e70b8-126">Поставщик услуг для этого устройства должен реализовать интерфейс IMDServiceProvider2.</span><span class="sxs-lookup"><span data-stu-id="e70b8-126">The service provider for this device must implement the IMDServiceProvider2 interface.</span></span>
-   <span data-ttu-id="e70b8-127">Ключ поставщика услуг в разделе HKEY \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows Media Диспетчер устройств \\ plugins \\ SP \\ "имя пакета обновления" должен содержать следующее значение DWORD</span><span class="sxs-lookup"><span data-stu-id="e70b8-127">The service provider key under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\Plugins\\SP\\SPName must contain the following DWORD value</span></span>
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a><span data-ttu-id="e70b8-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e70b8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e70b8-129">**Создание поставщика услуг**</span><span class="sxs-lookup"><span data-stu-id="e70b8-129">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




