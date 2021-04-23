---
title: Интерфейс Ибасикдевице
description: Инкапсулирует методы и события, необходимые для моделирования устройства DLNA.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- API потоковой передачи мультимедиа интерфейса Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, описание
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1567605fb160fc69ac933bb94a0b0282e35616d5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2020
ms.locfileid: "104414116"
---
# <a name="ibasicdevice-interface"></a><span data-ttu-id="529cd-105">Интерфейс Ибасикдевице</span><span class="sxs-lookup"><span data-stu-id="529cd-105">IBasicDevice interface</span></span>

<span data-ttu-id="529cd-106">Инкапсулирует методы и события, необходимые для моделирования устройства DLNA.</span><span class="sxs-lookup"><span data-stu-id="529cd-106">Encapsulates the methods and events needed to model a DLNA Device.</span></span>

## <a name="members"></a><span data-ttu-id="529cd-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="529cd-107">Members</span></span>

<span data-ttu-id="529cd-108">Интерфейс **ибасикдевице** наследует от [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="529cd-108">The **IBasicDevice** interface inherits from [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="529cd-109">**Ибасикдевице** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="529cd-109">**IBasicDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="529cd-110">Методы</span><span class="sxs-lookup"><span data-stu-id="529cd-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="529cd-111">Методы</span><span class="sxs-lookup"><span data-stu-id="529cd-111">Methods</span></span>

<span data-ttu-id="529cd-112">Интерфейс **ибасикдевице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="529cd-112">The **IBasicDevice** interface has these methods.</span></span>



| <span data-ttu-id="529cd-113">Метод</span><span class="sxs-lookup"><span data-stu-id="529cd-113">Method</span></span>                                                                                 | <span data-ttu-id="529cd-114">Описание</span><span class="sxs-lookup"><span data-stu-id="529cd-114">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="529cd-115">**добавить \_ коннектионстатусчанжед**</span><span class="sxs-lookup"><span data-stu-id="529cd-115">**add\_ConnectionStatusChanged**</span></span>](ibasicdevice-add-connectionstatuschanged.md)       | <span data-ttu-id="529cd-116">Регистрирует обработчик событий для события [**коннектионстатусчанжед**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="529cd-116">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>                |
| [<span data-ttu-id="529cd-117">**канвакедевицес**</span><span class="sxs-lookup"><span data-stu-id="529cd-117">**CanWakeDevices**</span></span>](ibasicdevice-canwakedevices.md)                                  | <span data-ttu-id="529cd-118">Возвращает значение, указывающее, может ли устройство пробудиться.</span><span class="sxs-lookup"><span data-stu-id="529cd-118">Retrieves a value that indicates if the device can wake.</span></span><br/>                                                            |
| <span data-ttu-id="529cd-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="529cd-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span></span>                              | <span data-ttu-id="529cd-120">Возвращает значение перечисления, указывающее, находится ли устройство в данный момент в режиме «вне линии», в состоянии «в наличии», а также через режим пробуждения.</span><span class="sxs-lookup"><span data-stu-id="529cd-120">Returns an enumeration value indicating whether the device is currently on-line, off-line or sleeping but wakeable.</span></span><br/> |
| [<span data-ttu-id="529cd-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="529cd-121">**Description**</span></span>](ibasicdevice-description.md)                                        | <span data-ttu-id="529cd-122">Извлекает описание устройства.</span><span class="sxs-lookup"><span data-stu-id="529cd-122">Retrieves a description of the device.</span></span><br/>                                                                              |
| [<span data-ttu-id="529cd-123">**дисковередонкуррентнетворк**</span><span class="sxs-lookup"><span data-stu-id="529cd-123">**DiscoveredOnCurrentNetwork**</span></span>](ibasicdevice-discoveredoncurrentnetwork.md)          | <span data-ttu-id="529cd-124">Возвращает значение, указывающее, находится ли устройство в текущей сети.</span><span class="sxs-lookup"><span data-stu-id="529cd-124">Retrieves a value that indicates if the device is on the current network.</span></span><br/>                                           |
| [<span data-ttu-id="529cd-125">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="529cd-125">**FriendlyName**</span></span>](ibasicdevice-friendlyname.md)                                      | <span data-ttu-id="529cd-126">Получает понятное имя устройства s.</span><span class="sxs-lookup"><span data-stu-id="529cd-126">Retrieves the device s friendly name.</span></span><br/>                                                                               |
| [<span data-ttu-id="529cd-127">**Значки**</span><span class="sxs-lookup"><span data-stu-id="529cd-127">**Icons**</span></span>](ibasicdevice-icons.md)                                                    | <span data-ttu-id="529cd-128">Возвращает вектор интерфейсов [**идевицеикон**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="529cd-128">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span><br/>                                                  |
| [<span data-ttu-id="529cd-129">**IpAddresses**</span><span class="sxs-lookup"><span data-stu-id="529cd-129">**IpAddresses**</span></span>](ibasicdevice-ipaddresses.md)                                        | <span data-ttu-id="529cd-130">Возвращает вектор IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="529cd-130">Returns a vector of IP addresses.</span></span><br/>                                                                                   |
| [<span data-ttu-id="529cd-131">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="529cd-131">**ManufacturerName**</span></span>](ibasicdevice-manufacturername.md)                              | <span data-ttu-id="529cd-132">Получает имя изготовителя устройства.</span><span class="sxs-lookup"><span data-stu-id="529cd-132">Retrieves the device s manufacturer name.</span></span><br/>                                                                           |
| [<span data-ttu-id="529cd-133">**мануфактурерурл**</span><span class="sxs-lookup"><span data-stu-id="529cd-133">**ManufacturerUrl**</span></span>](ibasicdevice-manufacturerurl.md)                                | <span data-ttu-id="529cd-134">Получает URL-адрес изготовителя устройства.</span><span class="sxs-lookup"><span data-stu-id="529cd-134">Retrieves the device s manufacturer URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="529cd-135">**ModelName**</span><span class="sxs-lookup"><span data-stu-id="529cd-135">**ModelName**</span></span>](ibasicdevice-modelname.md)                                            | <span data-ttu-id="529cd-136">Извлекает имя модели устройства s.</span><span class="sxs-lookup"><span data-stu-id="529cd-136">Retrieves the device s model name.</span></span><br/>                                                                                  |
| [<span data-ttu-id="529cd-137">**ModelNumber**</span><span class="sxs-lookup"><span data-stu-id="529cd-137">**ModelNumber**</span></span>](ibasicdevice-modelnumber.md)                                        | <span data-ttu-id="529cd-138">Извлекает номер модели устройства s.</span><span class="sxs-lookup"><span data-stu-id="529cd-138">Retrieves the device s model number.</span></span><br/>                                                                                |
| [<span data-ttu-id="529cd-139">**моделурл**</span><span class="sxs-lookup"><span data-stu-id="529cd-139">**ModelUrl**</span></span>](ibasicdevice-modelurl.md)                                              | <span data-ttu-id="529cd-140">Извлекает URL-адрес модели устройства s.</span><span class="sxs-lookup"><span data-stu-id="529cd-140">Retrieves the device s model URL.</span></span><br/>                                                                                   |
| [<span data-ttu-id="529cd-141">**фисикаладдрессес**</span><span class="sxs-lookup"><span data-stu-id="529cd-141">**PhysicalAddresses**</span></span>](ibasicdevice-physicaladdresses.md)                            | <span data-ttu-id="529cd-142">Возвращает вектор физических адресов.</span><span class="sxs-lookup"><span data-stu-id="529cd-142">Returns a vector of physical addresses.</span></span><br/>                                                                             |
| [<span data-ttu-id="529cd-143">**пресентатионурл**</span><span class="sxs-lookup"><span data-stu-id="529cd-143">**PresentationUrl**</span></span>](ibasicdevice-presentationurl.md)                                | <span data-ttu-id="529cd-144">Извлекает URL-адрес презентации устройства с.</span><span class="sxs-lookup"><span data-stu-id="529cd-144">Retrieves the device s presentation URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="529cd-145">**ремотестреамингурлс**</span><span class="sxs-lookup"><span data-stu-id="529cd-145">**RemoteStreamingUrls**</span></span>](ibasicdevice-remotestreamingurls.md)                        | <span data-ttu-id="529cd-146">Возвращает вектор URL-адресов удаленной потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="529cd-146">Returns a vector of remote streaming URLs.</span></span><br/>                                                                          |
| [<span data-ttu-id="529cd-147">**удалить \_ коннектионстатусчанжед**</span><span class="sxs-lookup"><span data-stu-id="529cd-147">**remove\_ConnectionStatusChanged**</span></span>](ibasicdevice-remove-connectionstatuschanged.md) | <span data-ttu-id="529cd-148">Отменяет регистрацию обработчика событий для события [**коннектионстатусчанжед**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="529cd-148">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>              |
| [<span data-ttu-id="529cd-149">**Номер**</span><span class="sxs-lookup"><span data-stu-id="529cd-149">**SerialNumber**</span></span>](ibasicdevice-serialnumber.md)                                      | <span data-ttu-id="529cd-150">Извлекает серийный номер устройства s.</span><span class="sxs-lookup"><span data-stu-id="529cd-150">Retrieves the device s serial number.</span></span><br/>                                                                               |
| [<span data-ttu-id="529cd-151">**Тип**</span><span class="sxs-lookup"><span data-stu-id="529cd-151">**Type**</span></span>](ibasicdevice-type.md)                                                      | <span data-ttu-id="529cd-152">Возвращает значение перечисления, указывающее тип устройства DLNA.</span><span class="sxs-lookup"><span data-stu-id="529cd-152">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span><br/>                                       |
| [<span data-ttu-id="529cd-153">**уникуедевиценаме**</span><span class="sxs-lookup"><span data-stu-id="529cd-153">**UniqueDeviceName**</span></span>](ibasicdevice-uniquedevicename.md)                              | <span data-ttu-id="529cd-154">Извлекает уникальное имя устройства (УДН) устройства.</span><span class="sxs-lookup"><span data-stu-id="529cd-154">Retrieves the device s unique device name (UDN).</span></span><br/>                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="529cd-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="529cd-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="529cd-156">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="529cd-156">**IInspectable**</span></span>](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

