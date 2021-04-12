---
description: В этом справочнике по программированию для пакета Audio SDK содержатся следующие свойства.
ms.assetid: db7d68c3-5642-4238-a212-88d3479ce73d
title: Основные свойства звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41528e66977f1f3b9282cf78ba76e4bae32c5bd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538321"
---
# <a name="core-audio-properties"></a><span data-ttu-id="d8fef-103">Основные свойства звука</span><span class="sxs-lookup"><span data-stu-id="d8fef-103">Core Audio Properties</span></span>

<span data-ttu-id="d8fef-104">В этом справочнике по программированию для пакета Audio SDK содержатся следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d8fef-104">This programming reference for the Core Audio SDK includes the following properties.</span></span>

## <a name="audio-endpoint-properties"></a><span data-ttu-id="d8fef-105">Свойства конечной точки аудио</span><span class="sxs-lookup"><span data-stu-id="d8fef-105">Audio Endpoint Properties</span></span>

<span data-ttu-id="d8fef-106">Core Audio SDK включает несколько свойств [устройств конечных точек звука](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="d8fef-106">Core Audio SDK includes several properties of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="d8fef-107">Дополнительные сведения см. в разделе [свойства конечной точки аудио](audio-endpoint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d8fef-107">For more information, see [Audio Endpoint Properties](audio-endpoint-properties.md).</span></span>

<span data-ttu-id="d8fef-108">Следующие свойства определяются в Ммдевицеапи. h в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="d8fef-108">The following properties are defined in Mmdeviceapi.h in Windows Vista and later.</span></span>



| <span data-ttu-id="d8fef-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="d8fef-109">Property</span></span>                                                                                                            | <span data-ttu-id="d8fef-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d8fef-110">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8fef-111">**\_Связь АУДИОЕНДПОИНТ \_ PKEY**</span><span class="sxs-lookup"><span data-stu-id="d8fef-111">**PKEY\_AudioEndpoint\_Association**</span></span>](pkey-audioendpoint-association.md)                                          | <span data-ttu-id="d8fef-112">Связывает категорию закрепления ядра (KS) с устройством конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="d8fef-112">Associates a kernel-streaming (KS) pin category with an audio endpoint device.</span></span>                                                                                |
| [<span data-ttu-id="d8fef-113">**PKEY \_ аудиоендпоинт \_ контролпанелпажепровидер**</span><span class="sxs-lookup"><span data-stu-id="d8fef-113">**PKEY\_AudioEndpoint\_ControlPanelPageProvider**</span></span>](pkey-audioendpoint-controlpanelpageprovider.md)                | <span data-ttu-id="d8fef-114">Указывает идентификатор CLSID зарегистрированного поставщика расширения свойств устройства для устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="d8fef-114">Specifies the CLSID of the registered provider of the device-properties extension for the audio endpoint device.</span></span>                                              |
| [<span data-ttu-id="d8fef-115">**PKEY \_ аудиоендпоинт \_ Отключить \_ сисфкс**</span><span class="sxs-lookup"><span data-stu-id="d8fef-115">**PKEY\_AudioEndpoint\_Disable\_SysFx**</span></span>](pkey-audioendpoint-disable-sysfx.md)                                     | <span data-ttu-id="d8fef-116">Указывает, включены ли системные эффекты в потоке общего режима, который передается на устройство конечной точки аудио или с него.</span><span class="sxs-lookup"><span data-stu-id="d8fef-116">Indicates whether system effects are enabled in the shared-mode stream that flows to or from the audio endpoint device.</span></span>                                       |
| [<span data-ttu-id="d8fef-117">**PKEY \_ аудиоендпоинт \_ формфактор**</span><span class="sxs-lookup"><span data-stu-id="d8fef-117">**PKEY\_AudioEndpoint\_FormFactor**</span></span>](pkey-audioendpoint-formfactor.md)                                            | <span data-ttu-id="d8fef-118">Указывает физические атрибуты устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="d8fef-118">Indicates the physical attributes of the audio endpoint device.</span></span>                                                                                               |
| [<span data-ttu-id="d8fef-119">**PKEY \_ аудиоендпоинт \_ фуллранжеспеакерс**</span><span class="sxs-lookup"><span data-stu-id="d8fef-119">**PKEY\_AudioEndpoint\_FullRangeSpeakers**</span></span>](pkey-audioendpoint-fullrangespeakers.md)                              | <span data-ttu-id="d8fef-120">Указывает маску конфигурации канала для всех динамиков с полным диапазоном, подключенных к устройству конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="d8fef-120">Specifies the channel-configuration mask for the full-range speakers that are connected to the audio endpoint device.</span></span>                                         |
| [<span data-ttu-id="d8fef-121">**\_Идентификатор PKEY аудиоендпоинт \_**</span><span class="sxs-lookup"><span data-stu-id="d8fef-121">**PKEY\_AudioEndpoint\_GUID**</span></span>](pkey-audioendpoint-guid.md)                                                        | <span data-ttu-id="d8fef-122">Предоставляет идентификатор устройства DirectSound, соответствующий устройству конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="d8fef-122">Supplies the DirectSound device identifier that corresponds to the audio endpoint device.</span></span>                                                                     |
| [<span data-ttu-id="d8fef-123">**PKEY \_ аудиоендпоинт \_ фисикалспеакерс**</span><span class="sxs-lookup"><span data-stu-id="d8fef-123">**PKEY\_AudioEndpoint\_PhysicalSpeakers**</span></span>](pkey-audioendpoint-physicalspeakers.md)                                | <span data-ttu-id="d8fef-124">Определяет конфигурацию физического динамика для устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="d8fef-124">Defines the physical speaker configuration for the audio endpoint device.</span></span>                                                                                     |
| [<span data-ttu-id="d8fef-125">**PKEY \_ аудиоенгине \_ девицеформат**</span><span class="sxs-lookup"><span data-stu-id="d8fef-125">**PKEY\_AudioEngine\_DeviceFormat**</span></span>](pkey-audioengine-deviceformat.md)                                            | <span data-ttu-id="d8fef-126">Указывает формат устройства, который используется подсистемой аудио для потока общего режима, который передается на устройство конечной точки аудио или с него.</span><span class="sxs-lookup"><span data-stu-id="d8fef-126">Specifies the device format, which is the format that the audio engine uses for the shared-mode stream that flows to or from the audio endpoint device.</span></span>       |
| [<span data-ttu-id="d8fef-127">**PKEY \_ аудиоенгине \_ оемформат**</span><span class="sxs-lookup"><span data-stu-id="d8fef-127">**PKEY\_AudioEngine\_OEMFormat**</span></span>](pkey-audioengine-oemformat.md)<br/>                                       | <span data-ttu-id="d8fef-128">Задает формат по умолчанию для устройства, используемого для отрисовки или записи потока.</span><span class="sxs-lookup"><span data-stu-id="d8fef-128">Specifies the default format of the device that is used for rendering or capturing a stream.</span></span> <span data-ttu-id="d8fef-129">Значения заполняются поставщиком вычислительной техники в INF-файле.</span><span class="sxs-lookup"><span data-stu-id="d8fef-129">The values are populated by the OEM in an .inf file.</span></span> <br/> |
| [<span data-ttu-id="d8fef-130">**PKEY \_ аудиоендпоинт \_ поддерживает \_ \_ режим EventDriven**</span><span class="sxs-lookup"><span data-stu-id="d8fef-130">**PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode**</span></span>](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | <span data-ttu-id="d8fef-131">Указывает, поддерживает ли конечная точка режим, управляемый событиями.</span><span class="sxs-lookup"><span data-stu-id="d8fef-131">Indicates whether the endpoint supports the event-driven mode.</span></span> <span data-ttu-id="d8fef-132">Значения заполняются поставщиком вычислительной техники в INF-файле.</span><span class="sxs-lookup"><span data-stu-id="d8fef-132">The values are populated by the OEM in an .inf file.</span></span><br/>                                |
| [<span data-ttu-id="d8fef-133">**PKEY \_ аудиоендпоинт \_ жакксубтипе**</span><span class="sxs-lookup"><span data-stu-id="d8fef-133">**PKEY\_AudioEndpoint\_JackSubType**</span></span>](pkey-audioendpoint-jacksubtype.md)<br/>                               | <span data-ttu-id="d8fef-134">Содержит идентификатор GUID категории выходных данных для устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="d8fef-134">Contains an output category GUID for an audio endpoint device.</span></span> <br/>                                                                                    |



 

## <a name="device-properties"></a><span data-ttu-id="d8fef-135">Свойства устройства</span><span class="sxs-lookup"><span data-stu-id="d8fef-135">Device Properties</span></span>

<span data-ttu-id="d8fef-136">Пакет SDK для аудиоподсистемы Core включает несколько свойств устройства для [устройств конечных точек аудио](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="d8fef-136">Core Audio SDK includes several device properties of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="d8fef-137">Дополнительные сведения см. в разделе [Свойства устройства](device-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d8fef-137">For more information, see [Device Properties](device-properties.md).</span></span>

<span data-ttu-id="d8fef-138">Следующие свойства определены в Функтиондисковерикэйс \_ девпкэй. h в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="d8fef-138">The following properties are defined in Functiondiscoverykeys\_devpkey.h in Windows Vista and later.</span></span>



| <span data-ttu-id="d8fef-139">Свойство</span><span class="sxs-lookup"><span data-stu-id="d8fef-139">Property</span></span>                                                                         | <span data-ttu-id="d8fef-140">Описание</span><span class="sxs-lookup"><span data-stu-id="d8fef-140">Description</span></span>                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8fef-141">**PKEY \_ девицеинтерфаце \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="d8fef-141">**PKEY\_DeviceInterface\_FriendlyName**</span></span>](pkey-deviceinterface-friendlyname.md) | <span data-ttu-id="d8fef-142">Понятное имя звукового адаптера, к которому подключено устройство конечной точки (например, "XYZ Audio Adapter").</span><span class="sxs-lookup"><span data-stu-id="d8fef-142">The friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span>                                                                               |
| [<span data-ttu-id="d8fef-143">**\_Девицедеск устройства \_ PKEY**</span><span class="sxs-lookup"><span data-stu-id="d8fef-143">**PKEY\_Device\_DeviceDesc**</span></span>](pkey-device-devicedesc.md)                       | <span data-ttu-id="d8fef-144">Описание устройства конечной точки (например, "динамики").</span><span class="sxs-lookup"><span data-stu-id="d8fef-144">The device description of the endpoint device (for example, "Speakers").</span></span>                                                                                                                          |
| [<span data-ttu-id="d8fef-145">**PKEY \_ устройство \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="d8fef-145">**PKEY\_Device\_FriendlyName**</span></span>](pkey-device-friendlyname.md)                   | <span data-ttu-id="d8fef-146">Понятное имя устройства конечной точки (например, "динамики (аудио-адаптер XYZ)").</span><span class="sxs-lookup"><span data-stu-id="d8fef-146">The friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span>                                                                                                           |
| <span data-ttu-id="d8fef-147">**\_Драйвер PKEY устройства \_ ContainerId**</span><span class="sxs-lookup"><span data-stu-id="d8fef-147">**PKEY\_Device\_ContainerId**</span></span>                                                    | <span data-ttu-id="d8fef-148">Хранит идентификатор контейнера устройства PnP, реализующего конечную точку аудио.</span><span class="sxs-lookup"><span data-stu-id="d8fef-148">Stores the container identifier of the PnP device that implements the audio endpoint.</span></span> <span data-ttu-id="d8fef-149">Дополнительные сведения об этом свойстве см. в разделе "Справочник по свойствам устройства" в документации по Windows WDK.</span><span class="sxs-lookup"><span data-stu-id="d8fef-149">For more information about this property, see "Device Property Reference" in the Windows WDK documentation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d8fef-150">См. также</span><span class="sxs-lookup"><span data-stu-id="d8fef-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8fef-151">Справочник по программированию</span><span class="sxs-lookup"><span data-stu-id="d8fef-151">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




