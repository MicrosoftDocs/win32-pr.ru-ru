---
description: API Ендпоинтволуме
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: API Ендпоинтволуме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b827045250336aa499e386a8dafedb6ae068b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807564"
---
# <a name="endpointvolume-api"></a><span data-ttu-id="d5988-103">API Ендпоинтволуме</span><span class="sxs-lookup"><span data-stu-id="d5988-103">EndpointVolume API</span></span>

<span data-ttu-id="d5988-104">API Ендпоинтволуме позволяет специализированным клиентам управлять уровнями громкости [конечных точек аудио](audio-endpoint-devices.md)и отслеживать их.</span><span class="sxs-lookup"><span data-stu-id="d5988-104">The EndpointVolume API enables specialized clients to control and monitor the volume levels of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="d5988-105">Клиент получает ссылки на интерфейсы в API Ендпоинтволуме, получая интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) устройства конечной точки аудио и вызывая метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) .</span><span class="sxs-lookup"><span data-stu-id="d5988-105">A client obtains references to the interfaces in the EndpointVolume API by obtaining the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an audio endpoint device and calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method.</span></span>

<span data-ttu-id="d5988-106">Файл заголовка Ендпоинтволуме. h определяет интерфейсы в API Ендпоинтволуме.</span><span class="sxs-lookup"><span data-stu-id="d5988-106">Header file Endpointvolume.h defines the interfaces in the EndpointVolume API.</span></span>

<span data-ttu-id="d5988-107">Звуковые приложения, использующие [API ммдевице](mmdevice-api.md) и [васапи](wasapi.md) , обычно используют интерфейс [**исимплеаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) для управления уровнями громкости на основе каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="d5988-107">Audio applications that use the [MMDevice API](mmdevice-api.md) and [WASAPI](wasapi.md) typically use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interface to control volume levels on a per-session basis.</span></span> <span data-ttu-id="d5988-108">Только два типа звуковых приложений нуждаются в использовании API Ендпоинтволуме.</span><span class="sxs-lookup"><span data-stu-id="d5988-108">Only two types of audio applications require the use of the EndpointVolume API.</span></span> <span data-ttu-id="d5988-109">Эти типы приложений:</span><span class="sxs-lookup"><span data-stu-id="d5988-109">These application types are:</span></span>

-   <span data-ttu-id="d5988-110">Приложения, управляющие основными уровнями громкости конечных точек аудио, аналогичны программе Windows Volume Control, Sndvol.exe.</span><span class="sxs-lookup"><span data-stu-id="d5988-110">Applications that manage the master volume levels of audio endpoint devices, similar to the Windows volume-control program, Sndvol.exe.</span></span>
-   <span data-ttu-id="d5988-111">Профессиональные приложения аудио ("Pro Audio"), требующие монопольного доступа к устройствам конечных точек аудио.</span><span class="sxs-lookup"><span data-stu-id="d5988-111">Professional audio ("pro audio") applications that require exclusive-mode access to audio endpoint devices.</span></span>

<span data-ttu-id="d5988-112">Неправильное использование API Ендпоинтволуме может повлиять на политику Windows Audio и нарушить параметры системного тома пользователя.</span><span class="sxs-lookup"><span data-stu-id="d5988-112">Inappropriate use of the EndpointVolume API can interfere with Windows audio policy and disrupt the user's system volume settings.</span></span>

<span data-ttu-id="d5988-113">Если устройство конечной точки звука реализует аппаратный том и выключает элементы управления, API Ендпоинтволуме использует эти элементы управления для управления томом устройства.</span><span class="sxs-lookup"><span data-stu-id="d5988-113">If an audio endpoint device implements hardware volume and mute controls, the EndpointVolume API uses those controls to manage the device volume.</span></span> <span data-ttu-id="d5988-114">В противном случае API Ендпоинтволуме реализует элементы управления в программном обеспечении прозрачно для клиента.</span><span class="sxs-lookup"><span data-stu-id="d5988-114">Otherwise, the EndpointVolume API implements the controls in software, transparently to the client.</span></span>

<span data-ttu-id="d5988-115">Если на устройстве есть аппаратный том и отключены элементы управления, изменения, внесенные в том устройства и отключения параметров через API Ендпоинтволуме, влияют на уровень громкости в общем и монопольном режимах.</span><span class="sxs-lookup"><span data-stu-id="d5988-115">If a device has hardware volume and mute controls, changes made to the device's volume and mute settings through the EndpointVolume API affect the volume level in both shared mode and exclusive mode.</span></span> <span data-ttu-id="d5988-116">Если на устройстве отсутствует аппаратный том и отключены элементы управления, изменения, внесенные в программный том и отключения элементов управления через API Ендпоинтволуме, влияют на уровень громкости в общем режиме, но не в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="d5988-116">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through the EndpointVolume API affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="d5988-117">В монопольном режиме клиент и устройство обмениваются данными напрямую, минуя элементы управления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="d5988-117">In exclusive mode, the client and the device exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="d5988-118">Для приложений, которые должны управлять томом оборудования и отключить элементы управления, API Ендпоинтволуме предлагает два потенциальных преимущества по сравнению с [API девицетопологи](devicetopology-api.md).</span><span class="sxs-lookup"><span data-stu-id="d5988-118">For applications that must manage hardware volume and mute controls, the EndpointVolume API offers two potential advantages over the [DeviceTopology API](devicetopology-api.md).</span></span>

<span data-ttu-id="d5988-119">Во-первых, ряд устройств аудио адаптеров не имеет аппаратных средств управления громкостью.</span><span class="sxs-lookup"><span data-stu-id="d5988-119">First, a number of audio adapter devices lack hardware volume controls.</span></span> <span data-ttu-id="d5988-120">Если на устройстве отсутствует аппаратный регулятор громкости, интерфейс [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) в API ендпоинтволуме автоматически реализует программный регулятор громкости для потока на этом устройстве или с него.</span><span class="sxs-lookup"><span data-stu-id="d5988-120">If a device lacks a hardware volume control, the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the EndpointVolume API automatically implements a software volume control on the stream to or from that device.</span></span> <span data-ttu-id="d5988-121">Для клиента API Ендпоинтволуме результат аналогичен тому, реализован ли на устройстве или в программном обеспечении с помощью интерфейса API Ендпоинтволуме.</span><span class="sxs-lookup"><span data-stu-id="d5988-121">For a client of the EndpointVolume API, the result is the same whether the volume control is implemented in hardware by the device or in software by the EndpointVolume API interface.</span></span>

<span data-ttu-id="d5988-122">Во-вторых, даже если устройство адаптера реализует аппаратные регуляторы громкости, приложение, использующее API Девицетопологи для реализации алгоритма обхода топологии, может не найти искомый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="d5988-122">Second, even if the adapter device does implement hardware volume controls, an application that uses the DeviceTopology API to implement a topology-traversal algorithm might fail to find the control that it is looking for.</span></span> <span data-ttu-id="d5988-123">Как правило, такое приложение предназначено для обхода топологии оборудования определенного устройства или набора связанных устройств.</span><span class="sxs-lookup"><span data-stu-id="d5988-123">Typically, such an application is designed to traverse the hardware topology of a particular device or set of related devices.</span></span> <span data-ttu-id="d5988-124">Приложение подвергается сбою, если оно пытается пройти по топологии устройства, которое не было специально разработано для или не тестировалось с помощью.</span><span class="sxs-lookup"><span data-stu-id="d5988-124">The application risks failing if it attempts to traverse the topology of a device that it has not been specifically designed for or tested with.</span></span>

<span data-ttu-id="d5988-125">Только специализированные приложения, которым требуется доступ к аппаратным функциям, отличным от тома, и отключения элементов управления должны использовать API Девицетопологи.</span><span class="sxs-lookup"><span data-stu-id="d5988-125">Only specialized applications that must access hardware functions other than volume and mute controls require the use of the DeviceTopology API.</span></span> <span data-ttu-id="d5988-126">Для приложений, которым требуется управлять только уровнем громкости потока с монопольным доступом, интерфейс API Ендпоинтволуме проще использовать и надежно работает с более широким спектром устройств звукового оборудования.</span><span class="sxs-lookup"><span data-stu-id="d5988-126">For applications that require control only of the volume level of an exclusive-mode stream, the EndpointVolume API is simpler to use and works reliably with a wider range of audio hardware devices.</span></span>

<span data-ttu-id="d5988-127">Примеры кода, в которых используются интерфейсы в API Ендпоинтволуме, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="d5988-127">For code examples that use the interfaces in the EndpointVolume API, see the following topics:</span></span>

-   [<span data-ttu-id="d5988-128">Элементы управления томами конечных точек</span><span class="sxs-lookup"><span data-stu-id="d5988-128">Endpoint Volume Controls</span></span>](endpoint-volume-controls.md)
-   [<span data-ttu-id="d5988-129">Пиковые показатели</span><span class="sxs-lookup"><span data-stu-id="d5988-129">Peak Meters</span></span>](peak-meters.md)

<span data-ttu-id="d5988-130">Пример, в котором используется API Ендпоинтволуме, см. в разделе [ендпоинтволуме](endpointvolume.md) в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d5988-130">To see a sample that uses the EndpointVolume API, see [EndpointVolume](endpointvolume.md) in the Windows SDK.</span></span>

<span data-ttu-id="d5988-131">API Ендпоинтволуме реализует следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="d5988-131">The EndpointVolume API implements the following interfaces.</span></span>



| <span data-ttu-id="d5988-132">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="d5988-132">Interface</span></span>                                                | <span data-ttu-id="d5988-133">Описание</span><span class="sxs-lookup"><span data-stu-id="d5988-133">Description</span></span>                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5988-134">**иаудиоендпоинтволуме**</span><span class="sxs-lookup"><span data-stu-id="d5988-134">**IAudioEndpointVolume**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | <span data-ttu-id="d5988-135">Представляет элементы управления громкостью в звуковом потоке на устройстве конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="d5988-135">Represents the volume controls on the audio stream to or from an audio endpoint device.</span></span> |
| [<span data-ttu-id="d5988-136">**иаудиометеринформатион**</span><span class="sxs-lookup"><span data-stu-id="d5988-136">**IAudioMeterInformation**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | <span data-ttu-id="d5988-137">Представляет пиковый счетчик звукового потока, на устройство конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="d5988-137">Represents a peak meter on the audio stream to or from an audio endpoint device.</span></span>        |



 

<span data-ttu-id="d5988-138">Кроме того, клиенты API Ендпоинтволуме, требующие уведомления тома и смены звука на устройствах конечных точек, должны реализовать следующий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d5988-138">In addition, clients of the EndpointVolume API that require notification of volume and muting changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="d5988-139">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="d5988-139">Interface</span></span>                                                            | <span data-ttu-id="d5988-140">Описание</span><span class="sxs-lookup"><span data-stu-id="d5988-140">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5988-141">**иаудиоендпоинтволумекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="d5988-141">**IAudioEndpointVolumeCallback**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | <span data-ttu-id="d5988-142">Предоставляет уведомления при изменении уровня громкости или выключения звука устройства конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d5988-142">Provides notifications when the volume level or muting state of an audio endpoint device changes.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d5988-143">См. также</span><span class="sxs-lookup"><span data-stu-id="d5988-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5988-144">Регуляторы громкости</span><span class="sxs-lookup"><span data-stu-id="d5988-144">Volume Controls</span></span>](volume-controls.md)
</dt> <dt>

[<span data-ttu-id="d5988-145">**Интерфейс Иммдевице**</span><span class="sxs-lookup"><span data-stu-id="d5988-145">**IMMDevice Interface**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="d5988-146">**Иммдевице:: Activate**</span><span class="sxs-lookup"><span data-stu-id="d5988-146">**IMMDevice::Activate**</span></span>](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[<span data-ttu-id="d5988-147">**исимплеаудиоволуме**</span><span class="sxs-lookup"><span data-stu-id="d5988-147">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[<span data-ttu-id="d5988-148">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="d5988-148">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



