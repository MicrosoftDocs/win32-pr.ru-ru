---
title: Параметры устройства
description: Параметры устройства
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Диспетчер устройств Windows Media, параметры устройства
- Диспетчер устройств, параметры устройства
- рекомендации по программированию, параметры устройств
- поставщики услуг, параметры устройства
- Создание поставщиков услуг, параметры устройства
- Параметры устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3ad1a1bfc6a24736fdad8385e6cc03e0b20be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329456"
---
# <a name="device-parameters"></a><span data-ttu-id="2630c-109">Параметры устройства</span><span class="sxs-lookup"><span data-stu-id="2630c-109">Device Parameters</span></span>

<span data-ttu-id="2630c-110">Диспетчер устройств Windows Media использует параметры устройства для управления поведением устройства.</span><span class="sxs-lookup"><span data-stu-id="2630c-110">Windows Media Device Manager uses device parameters to control the behavior of a device.</span></span> <span data-ttu-id="2630c-111">Эти параметры добавляются в реестр, как указано в файле установки устройства (INF-файле).</span><span class="sxs-lookup"><span data-stu-id="2630c-111">These parameters are added to the registry as specified in the device's installation file (INF file).</span></span> <span data-ttu-id="2630c-112">В следующей таблице перечислены параметры устройства, которые Windows Media диспетчер устройств запросы.</span><span class="sxs-lookup"><span data-stu-id="2630c-112">The following table lists the device parameters that Windows Media Device Manager queries.</span></span>



| <span data-ttu-id="2630c-113">Имя параметра устройства</span><span class="sxs-lookup"><span data-stu-id="2630c-113">Device parameter name</span></span> | <span data-ttu-id="2630c-114">Тип данных реестра</span><span class="sxs-lookup"><span data-stu-id="2630c-114">Registry data type</span></span> | <span data-ttu-id="2630c-115">Описание</span><span class="sxs-lookup"><span data-stu-id="2630c-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2630c-116">*вмдмспклсид*</span><span class="sxs-lookup"><span data-stu-id="2630c-116">*WMDMSPCLSID*</span></span>         | <span data-ttu-id="2630c-117">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="2630c-117">**REG\_SZ**</span></span>        | <span data-ttu-id="2630c-118">Значение, указывающее идентификатор CLSID поставщика услуг, управляющего этим устройством.</span><span class="sxs-lookup"><span data-stu-id="2630c-118">Value that specifies the CLSID of the service provider controlling this device.</span></span> <span data-ttu-id="2630c-119">Этот параметр является обязательным для поддержки PnP.</span><span class="sxs-lookup"><span data-stu-id="2630c-119">This parameter is mandatory for PnP support.</span></span><br/> <span data-ttu-id="2630c-120">Значение параметра должно быть идентификатором CLSID, а не ProgID поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="2630c-120">The parameter value must be the CLSID, not the ProgID of the service provider.</span></span> <span data-ttu-id="2630c-121">Этот параметр является обязательным для поддержки самонастраивающийся (PnP) в Windows Media диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="2630c-121">This parameter is mandatory to support Plug and Play (PnP) under Windows Media Device Manager.</span></span> <span data-ttu-id="2630c-122">Дополнительные сведения см. в разделе [Включение PnP для устройств](enabling-pnp-for-devices.md).</span><span class="sxs-lookup"><span data-stu-id="2630c-122">For more information, see [Enabling PnP for Devices](enabling-pnp-for-devices.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2630c-123">*оптималтрансферсизе*</span><span class="sxs-lookup"><span data-stu-id="2630c-123">*OptimalTransferSize*</span></span> | <span data-ttu-id="2630c-124">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2630c-124">**REG\_DWORD**</span></span>     | <span data-ttu-id="2630c-125">Необязательное значение, указывающее предпочтительный размер передачи, используемый Windows Media диспетчер устройств при операциях чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2630c-125">Optional value that specifies the preferred transfer size that Windows Media Device Manager uses during read and write operations.</span></span> <span data-ttu-id="2630c-126">Если он не указан, используется размер перемещения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2630c-126">If it is not supplied, a default transfer size is used.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2630c-127">*усеметадатавиевс*</span><span class="sxs-lookup"><span data-stu-id="2630c-127">*UseMetadataViews*</span></span>    | <span data-ttu-id="2630c-128">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2630c-128">**REG\_DWORD**</span></span>     | <span data-ttu-id="2630c-129">Необязательный параметр, указывающий, будет ли Windows Media диспетчер устройств упорядочивать содержимое по метаданным при представлении содержимого устройства в приложениях.</span><span class="sxs-lookup"><span data-stu-id="2630c-129">Optional parameter that specifies whether Windows Media Device Manager organizes the content by metadata while presenting device content to applications.</span></span> <span data-ttu-id="2630c-130">Если не указано, значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="2630c-130">If not specified, the default value is 0.</span></span><br/> <span data-ttu-id="2630c-131">Когда приложения перечисляют содержимое в хранилищах переносимого аудио-плеера, Windows Media диспетчер устройств может представлять содержимое, упорядоченное по метаданным.</span><span class="sxs-lookup"><span data-stu-id="2630c-131">When applications enumerate the content on the storages of a portable audio player, Windows Media Device Manager can present the content organized by metadata.</span></span> <span data-ttu-id="2630c-132">Это особенно удобно для устройств с большой емкостью хранилища.</span><span class="sxs-lookup"><span data-stu-id="2630c-132">This is especially useful for devices with large storage capacity.</span></span><br/> <span data-ttu-id="2630c-133">Приложения и устройства могут управлять этим поведением.</span><span class="sxs-lookup"><span data-stu-id="2630c-133">Applications and devices have the ability to control this behavior.</span></span> <span data-ttu-id="2630c-134">Устройства указывают свои предпочтения с помощью параметра устройства *усеметадатавиевс*.</span><span class="sxs-lookup"><span data-stu-id="2630c-134">Devices indicate their preference through the device parameter *UseMetadataViews*.</span></span><br/> <span data-ttu-id="2630c-135">Поддерживаются следующие два целочисленных значения:</span><span class="sxs-lookup"><span data-stu-id="2630c-135">The following two integer values are supported:</span></span><br/> <span data-ttu-id="2630c-136">Запрашивает, чтобы содержимое было представлено приложениям точно так же, как это было в файловой системе устройства.</span><span class="sxs-lookup"><span data-stu-id="2630c-136">Requests that content be presented to the applications exactly as organized on the file system of the device.</span></span><br/> <span data-ttu-id="2630c-137">Запрашивает, чтобы содержимое было представлено приложениям, упорядоченным по метаданным.</span><span class="sxs-lookup"><span data-stu-id="2630c-137">Requests that the content be presented to the applications organized by metadata.</span></span><br/> |
| <span data-ttu-id="2630c-138">*шовиншелл*</span><span class="sxs-lookup"><span data-stu-id="2630c-138">*ShowInShell*</span></span>         | <span data-ttu-id="2630c-139">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2630c-139">**REG\_DWORD**</span></span>     | <span data-ttu-id="2630c-140">Необязательный параметр, указывающий, должно ли устройство отображаться в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="2630c-140">Optional parameter that specifies whether the device should appear in Windows Explorer.</span></span> <span data-ttu-id="2630c-141">Значение 1 указывает, что устройство должно отображаться в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="2630c-141">The value 1 indicates that the device should appear in Windows Explorer.</span></span> <span data-ttu-id="2630c-142">Дополнительные сведения см. [в разделе Требования к портативным проигрывателям, отображаемым в проводнике Windows](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="2630c-142">For more information, see [Requirements for Portable Audio Players to Appear in Windows Explorer](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2630c-143">*усикстендедвмдм*</span><span class="sxs-lookup"><span data-stu-id="2630c-143">*UseExtendedWmdm*</span></span>     | <span data-ttu-id="2630c-144">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2630c-144">**REG\_DWORD**</span></span>     | <span data-ttu-id="2630c-145">Необязательный параметр, который оповещает Windows Media диспетчер устройств о том, что поставщик услуг поддерживает **IMDSPDevice3**, **IMDSPObject2** и **IMDSPStorage4**.</span><span class="sxs-lookup"><span data-stu-id="2630c-145">Optional parameter that alerts Windows Media Device Manager that the service provider supports **IMDSPDevice3**, **IMDSPObject2**, and **IMDSPStorage4**.</span></span> <span data-ttu-id="2630c-146">Без этого флага Windows Media диспетчер устройств не будет вызывать эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="2630c-146">Without this flag, Windows Media Device Manager will never call these interfaces.</span></span> <span data-ttu-id="2630c-147">Значение 1 указывает, что эти интерфейсы поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="2630c-147">The value 1 indicates that these interfaces are supported.</span></span><br/> <span data-ttu-id="2630c-148">Этот флаг необходим для поставщиков услуг, которые синхронизируются с проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2630c-148">This flag is required for service providers that synchronize with Windows Media Player.</span></span> <span data-ttu-id="2630c-149">(См. раздел [Включение синхронизации с помощью проигрывателя Windows Media](enabling-synchronization-with-windows-media-player.md)).</span><span class="sxs-lookup"><span data-stu-id="2630c-149">(See [Enabling Synchronization with Windows Media Player](enabling-synchronization-with-windows-media-player.md)).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="2630c-150">**Кодирование INF-файла**</span><span class="sxs-lookup"><span data-stu-id="2630c-150">**Coding the INF file**</span></span>

<span data-ttu-id="2630c-151">В следующем примере кода из INF-файла устройства демонстрируется настройка некоторых параметров устройства во время установки устройства.</span><span class="sxs-lookup"><span data-stu-id="2630c-151">The following example code from a device's INF file demonstrates setting some device parameters during device installation.</span></span>


```C++
; Set parameters on Windows 95 and Windows 98 operating systems.
[DriverInstall.hw]
AddReg=DriverHwPropReg

; Set parameters on Windows NT-based operating systems.
[DriverInstall.NT.hw]
AddReg=DriverHwPropReg

; Related section that specifies the device parameters.
[DriverHwPropReg]
; Add your own CLSID here.
HKR,,WMDMSPCLSID,,"{00000000-0000-0000-0000-000000000000}"
HKR,,OptimalTransferSize,0x10001,0x10000
HKR,,UseMetadataViews,0x10001,0x1
```



## <a name="related-topics"></a><span data-ttu-id="2630c-152">См. также</span><span class="sxs-lookup"><span data-stu-id="2630c-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2630c-153">**Создание поставщика услуг**</span><span class="sxs-lookup"><span data-stu-id="2630c-153">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="2630c-154">**Интерфейс IMDServiceProvider2**</span><span class="sxs-lookup"><span data-stu-id="2630c-154">**IMDServiceProvider2 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)
</dt> <dt>

[<span data-ttu-id="2630c-155">**IMDServiceProvider2:: Креатедевице**</span><span class="sxs-lookup"><span data-stu-id="2630c-155">**IMDServiceProvider2::CreateDevice**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice)
</dt> <dt>

[<span data-ttu-id="2630c-156">**Интерфейс Ивмдмдевице**</span><span class="sxs-lookup"><span data-stu-id="2630c-156">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





