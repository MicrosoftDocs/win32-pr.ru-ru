---
title: Перечисление устройств (ВМДМ)
description: Диспетчер устройств Windows Media поддерживает кэш подключенных устройств. Узнайте, как Windows Media диспетчер устройств поддерживает или обновляет свой кэш.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Диспетчер устройств Windows Media, перечисление устройств
- Диспетчер устройств, перечисление устройств
- программное содержимое, перечисление устройств
- поставщики услуг, перечисление устройств
- Создание поставщиков услуг, перечисление устройств
- Перечисление устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9b2fd3a891e2c52710bd9a2f6d46a78e9eb238
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112067911"
---
# <a name="enumerating-devices-wmdm"></a><span data-ttu-id="68323-110">Перечисление устройств (ВМДМ)</span><span class="sxs-lookup"><span data-stu-id="68323-110">Enumerating devices (WMDM)</span></span>

<span data-ttu-id="68323-111">Диспетчер устройств Windows Media поддерживает кэш подключенных устройств, которые обновляются при запуске приложения диспетчер устройств Windows Media, при подключении или отключении устройства самонастраивающийся (PnP) или при вызове [**IWMDeviceManager2:: Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span><span class="sxs-lookup"><span data-stu-id="68323-111">Windows Media Device Manager maintains a cache of connected devices that is updated when a Windows Media Device Manager application starts, when a Plug and Play (PnP) device connects or disconnects, or when the application calls [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span></span> <span data-ttu-id="68323-112">Этот кэш предоставляется приложению при вызове [**ивмдевицеманажер:: енумдевицес**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) или [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span><span class="sxs-lookup"><span data-stu-id="68323-112">This cache is exposed to the application when it calls [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) or [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span></span> <span data-ttu-id="68323-113">Каждое устройство предоставляется приложению как интерфейс [**ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="68323-113">Each device is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="68323-114">Если поставщик услуг зарегистрирован для работы с устройствами PnP, Windows Media диспетчер устройств будет знать о текущем списке подключенных устройств.</span><span class="sxs-lookup"><span data-stu-id="68323-114">If the service provider is registered to handle PnP devices, Windows Media Device Manager will be aware of the current list of connected devices.</span></span> <span data-ttu-id="68323-115">Если поставщик услуг зарегистрирован для управления устройствами, не поддерживающими PnP, поставщик услуг отвечает за обнаружение подключенных устройств.</span><span class="sxs-lookup"><span data-stu-id="68323-115">If the service provider is registered to handle non-PnP devices, the service provider is responsible for discovering attached devices.</span></span> <span data-ttu-id="68323-116">Поставщик услуг может быть зарегистрирован только для устройств PnP или не на основе PnP, но не в обоих случаях.</span><span class="sxs-lookup"><span data-stu-id="68323-116">A service provider can only be registered for PnP or non-PnP devices, never both.</span></span>

<span data-ttu-id="68323-117">Следующие действия показывают, как Windows Media диспетчер устройств поддерживает или обновляет свой кэш.</span><span class="sxs-lookup"><span data-stu-id="68323-117">The following actions show how Windows Media Device Manager maintains or updates its cache.</span></span> <span data-ttu-id="68323-118">Обратите внимание, что кэш никогда не обновляется при подключении или отключении устройства, не поддерживающего PnP.</span><span class="sxs-lookup"><span data-stu-id="68323-118">Notice that the cache is never updated when a non-PnP device connects or disconnects.</span></span>

<span data-ttu-id="68323-119">Запуск приложения диспетчер устройств Windows Media</span><span class="sxs-lookup"><span data-stu-id="68323-119">A Windows Media Device Manager application starts</span></span>

-   <span data-ttu-id="68323-120">Диспетчер устройств Windows Media извлекает список подключенных устройств PnP из подсистемы PnP и вызывает [**IMDServiceProvider2:: креатедевице**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) для служб SP, зарегистрированных для каждого подключенного устройства.</span><span class="sxs-lookup"><span data-stu-id="68323-120">Windows Media Device Manager retrieves a list of attached PnP devices from the PnP subsystem, and calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on the SP registered for each connected device.</span></span> <span data-ttu-id="68323-121">(Он обнаруживает правильного поставщика услуг, запрашивая параметр устройства ВМДМСПКЛСИД для идентификатора класса поставщика услуг, ответственного за это устройство.</span><span class="sxs-lookup"><span data-stu-id="68323-121">(It discovers the correct service provider by querying the WMDMSPCLSID device parameter for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="68323-122">Дополнительные сведения см. в разделе [Параметры устройства](device-parameters.md) .) Все возвращенные устройства добавляются в кэш Windows Media диспетчер устройств устройств.</span><span class="sxs-lookup"><span data-stu-id="68323-122">See [Device Parameters](device-parameters.md) for more information.) All devices returned are added to the Windows Media Device Manager cache of devices.</span></span>
-   <span data-ttu-id="68323-123">Windows Media диспетчер устройств находит все зарегистрированные в нем поставщики служб, не поддерживающих PnP, и вызывает [**имдсервицепровидер:: енумдевицес**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) для каждого поставщика услуг, чтобы получить список устройств от каждого из них.</span><span class="sxs-lookup"><span data-stu-id="68323-123">Windows Media Device Manager finds all non-PnP service providers registered with it and calls [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) on each service provider to get a list devices from each one.</span></span> <span data-ttu-id="68323-124">Все возвращенные устройства добавляются в кэш.</span><span class="sxs-lookup"><span data-stu-id="68323-124">All devices returned are added to the cache.</span></span>

<span data-ttu-id="68323-125">Приложение вызывает Ивмдевицеманажер/2:: Енумдевицес/2</span><span class="sxs-lookup"><span data-stu-id="68323-125">The application calls IWMDeviceManager/2::EnumDevices/2</span></span>

-   <span data-ttu-id="68323-126">Диспетчер устройств Windows Media возвращает свой список кэшированных устройств.</span><span class="sxs-lookup"><span data-stu-id="68323-126">Windows Media Device Manager returns its cached device list.</span></span>

<span data-ttu-id="68323-127">Устройство PnP подключается</span><span class="sxs-lookup"><span data-stu-id="68323-127">A PnP device connects</span></span>

-   <span data-ttu-id="68323-128">Windows Media диспетчер устройств находит соответствующего поставщика услуг и вызывает **IMDServiceProvider2:: креатедевице** и добавляет устройство в свой кэш.</span><span class="sxs-lookup"><span data-stu-id="68323-128">Windows Media Device Manager finds the relevant service provider and calls **IMDServiceProvider2::CreateDevice**, and adds the device to its cache.</span></span>
-   <span data-ttu-id="68323-129">Если приложение реализует [**ивмдмнотификатион**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Диспетчер устройств вызывает [**Ивмдмнотификатион:: вмдммессаже**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) с уведомлением о получении.</span><span class="sxs-lookup"><span data-stu-id="68323-129">If the application implements [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Device Manager calls [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) with an arrival notification.</span></span>

<span data-ttu-id="68323-130">PnP-устройство отключается</span><span class="sxs-lookup"><span data-stu-id="68323-130">A PnP device disconnects</span></span>

-   <span data-ttu-id="68323-131">Диспетчер устройств Windows Media удаляет элемент из кэша.</span><span class="sxs-lookup"><span data-stu-id="68323-131">Windows Media Device Manager removes the item from its cache.</span></span>
-   <span data-ttu-id="68323-132">Если приложение реализует Ивмдмнотификатион, Windows Media диспетчер устройств вызывает Ивмдмнотификатион:: Вмдммессаже с уведомлением о отправлении.</span><span class="sxs-lookup"><span data-stu-id="68323-132">If the application implements IWMDMNotification, Windows Media Device Manager calls IWMDMNotification::WMDMMessage with a departure notification.</span></span>

<span data-ttu-id="68323-133">Приложение вызывает IWMDeviceManager2:: Reinitialize</span><span class="sxs-lookup"><span data-stu-id="68323-133">The application calls IWMDeviceManager2::Reinitialize</span></span>

-   <span data-ttu-id="68323-134">Обновляет кэш всеми подключенными устройствами.</span><span class="sxs-lookup"><span data-stu-id="68323-134">Refreshes the cache with all connected devices.</span></span>

<span data-ttu-id="68323-135">Устройство, не поддерживающее PnP, подключается или отключается</span><span class="sxs-lookup"><span data-stu-id="68323-135">A non-PnP device connects or disconnects</span></span>

-   <span data-ttu-id="68323-136">Диспетчер устройств Windows Media не сообщает о поступлении или отправлении и не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="68323-136">Windows Media Device Manager is not informed of the arrival or departure, and takes no action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68323-137">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="68323-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68323-138">**Создание поставщика услуг**</span><span class="sxs-lookup"><span data-stu-id="68323-138">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




