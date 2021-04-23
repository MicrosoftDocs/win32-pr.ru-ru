---
description: Маршрутизация потоков — это способность приложения мультимедиа переключать потоки между устройствами с минимальным перерывом в воспроизведении или сеансе записи.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Потоковая маршрутизация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b21cd15a4467cb9b08747119aab999882ae3b5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496350"
---
# <a name="stream-routing"></a><span data-ttu-id="5c6ac-103">Потоковая маршрутизация</span><span class="sxs-lookup"><span data-stu-id="5c6ac-103">Stream Routing</span></span>

<span data-ttu-id="5c6ac-104">*Маршрутизация потоков* — это способность приложения мультимедиа переключать потоки между устройствами с минимальным перерывом в воспроизведении или сеансе записи.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-104">*Stream routing* is the ability of a media application to switch streams between devices with minimal interruption to the playback or the capture session.</span></span>

<span data-ttu-id="5c6ac-105">Компьютер может иметь несколько устройств отрисовки и записи.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-105">A computer can have multiple rendering and capture devices.</span></span> <span data-ttu-id="5c6ac-106">Система перечисляет эти устройства на панели управления " **звуки** ".</span><span class="sxs-lookup"><span data-stu-id="5c6ac-106">The system lists these devices on the **Sounds** control panel.</span></span> <span data-ttu-id="5c6ac-107">Из этого списка пользователь может задать устройство как устройство по умолчанию для каждой роли: воспроизведение, запись или четыре роли связи (визуализация консоли, захват консоли, Визуализация связи или захват связи).</span><span class="sxs-lookup"><span data-stu-id="5c6ac-107">From this list, a user can set a device to be the default device for each role: playback, recording, or the four communications roles (console render, console capture, communication render, or communication capture).</span></span> <span data-ttu-id="5c6ac-108">Список устройств может быть изменен динамически, так как некоторые из этих устройств могут быть временно доступны, например гарнитура USB.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-108">The list of devices may be modified dynamically as some of these devices can be available temporarily, for example a USB headset.</span></span> <span data-ttu-id="5c6ac-109">Если доступно несколько устройств, пользователь может изменить устройство по умолчанию на другое.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-109">When multiple devices are available, the user can change the default to a different device.</span></span> <span data-ttu-id="5c6ac-110">Пользователь также может изменить формат устройства (частота выборки, бит на выборку и т. д.) на вкладке **Дополнительно** для свойств устройства.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-110">The user can also change the format of a device (sample rate, bits per sample, and so on) on the **Advanced** tab for the device properties.</span></span>

<span data-ttu-id="5c6ac-111">Рассмотрим ситуацию, в которой пользователь выбирает **динамики** в качестве устройства по умолчанию для подготовки к просмотру звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-111">Consider a scenario in which a user selects **Speakers** as the default device for rendering audio streams.</span></span> <span data-ttu-id="5c6ac-112">Затем пользователь подключает гарнитуру USB, выбирает гарнитуру в качестве нового устройства по умолчанию и изменяет частоту дискретизации устройства с 44,1 кГц на 48 кГц.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-112">The user then connects a USB headset, selects the headset as the new default device, and changes the sample rate of the device from 44.1 kHz to 48 kHz.</span></span> <span data-ttu-id="5c6ac-113">Пользователь хочет воспроизвести аудиопоток на гарнитуре с новым темпом дискретизации с минимальным перерывом в сеансе потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-113">The user wants to play the audio stream on the headset at the new sample rate with minimal interruption to the streaming session.</span></span>

<span data-ttu-id="5c6ac-114">В этом сценарии существует два варианта, которые должны быть обработаны приложением мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="5c6ac-114">In this scenario, there are two cases that the media application must handle:</span></span>

-   <span data-ttu-id="5c6ac-115">Поток должен быть передан на новое устройство по умолчанию с минимальным перерывом в воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-115">The stream must be transferred to the new default device with minimal interruption to playback.</span></span>
-   <span data-ttu-id="5c6ac-116">Новое устройство должно возобновить воспроизведение в новом формате (то есть пользователь может изменить больше частоты выборки).</span><span class="sxs-lookup"><span data-stu-id="5c6ac-116">The new device must resume playback in the new format (that is, the user can change more than the sample rate).</span></span>

<span data-ttu-id="5c6ac-117">В Windows Vista для поддержки этого сценария приложению мультимедиа пришлось предоставить реализацию для потоковой маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-117">In Windows Vista, to support this scenario, the media application had to provide the implementation for stream routing.</span></span> <span data-ttu-id="5c6ac-118">Приложение было ответственным за завершение существующих потоков и перезапуск потоков на новом устройстве.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-118">The application was responsible for terminating existing streams and restarting the streams on the new device.</span></span> <span data-ttu-id="5c6ac-119">Если пользователь изменил устройство по умолчанию или изменил его формат Mix, все связанные сеансы были закрыты и приложению пришлось бы справиться с восстановлением.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-119">If the user changed the default device or its mix format changed, then all of the associated sessions were closed and the application had to handle the recovery.</span></span>

<span data-ttu-id="5c6ac-120">В Windows 7 приложение может легко передавать поток из существующего устройства по умолчанию в новую конечную точку звука по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-120">In Windows 7, an application can seamlessly transfer a stream from an existing default device to a new default audio endpoint.</span></span> <span data-ttu-id="5c6ac-121">Высокоуровневые наборы API аудио, такие как Media Foundation, DirectSound и WAVE API, реализуют функцию маршрутизации потоков.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-121">High-level audio API sets such as Media Foundation, DirectSound, and WAVE APIs implement the stream routing feature.</span></span> <span data-ttu-id="5c6ac-122">Приложения мультимедиа, использующие эти наборы API для воспроизведения или записи потока из устройства по умолчанию, используют реализацию по умолчанию и не должны изменять приложение.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-122">Media applications that use these API sets to play or capture a stream from the default device use the default implementation and will not have to modify the application.</span></span> <span data-ttu-id="5c6ac-123">Однако если приложение мультимедиа использует Ммдевицеапи или ВАСАПИ напрямую, приложение должно предоставить реализацию маршрутизации потоков.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-123">However, if your media application uses MMDeviceAPI or WASAPI directly, the application needs to provide the stream routing implementation.</span></span>

> [!Note]  
> <span data-ttu-id="5c6ac-124">Ммдевицеапи и ВАСАПИ — это основные компоненты API аудио, которые приложение может использовать для отображения или записи потока на устройстве.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-124">MMDeviceAPI and WASAPI are Core Audio API components that an application can use to render or capture a stream on a device.</span></span> <span data-ttu-id="5c6ac-125">Ммдевицеапи обнаруживает новое устройство конечной точки аудио, а ВАСАПИ управляет потоком звуковых данных между приложением мультимедиа и устройством конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-125">The MMDeviceAPI discovers the new audio endpoint device, and WASAPI manages the flow of audio data between a media application and the audio endpoint device.</span></span>

 

<span data-ttu-id="5c6ac-126">Чтобы реализовать функцию маршрутизации потоков, приложение должно прослушивать уведомления, отправленные Ммдевицеапи и ВАСАПИ, когда:</span><span class="sxs-lookup"><span data-stu-id="5c6ac-126">To implement the stream routing feature, the application must listen for the notifications sent by MMDeviceAPI and WASAPI when:</span></span>

-   <span data-ttu-id="5c6ac-127">Устройство по умолчанию изменяется пользователем.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-127">The default device is changed by the user.</span></span>
-   <span data-ttu-id="5c6ac-128">Существующее устройство по умолчанию удаляется, и добавляется новое устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-128">The existing default device is removed and a new default device is added.</span></span>
-   <span data-ttu-id="5c6ac-129">Формат устройства изменился.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-129">The device format is changed.</span></span>

<span data-ttu-id="5c6ac-130">Обрабатывая эти уведомления, приложение может выполнять необходимые операции управления потоками при передаче потока на новое устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-130">By handling these notifications, an application can perform the necessary stream management operations while transferring the stream to the new default device.</span></span> <span data-ttu-id="5c6ac-131">Кроме того, приложение может отображать или записывать существующие потоки, используя новый формат, заданный пользователем, пока активен сеанс отрисовки.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-131">In addition, the application can render or capture existing streams by using the new format specified by the user while a rendering session is active.</span></span>

<span data-ttu-id="5c6ac-132">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-132">This section contains the following topics:</span></span>

-   [<span data-ttu-id="5c6ac-133">Получение конечной точки устройства для маршрутизации потоков</span><span class="sxs-lookup"><span data-stu-id="5c6ac-133">Getting the Device Endpoint for Stream Routing</span></span>](getting-the-default-device-endpoint-for-stream-routing.md)
-   [<span data-ttu-id="5c6ac-134">Соответствующие уведомления для потоковой маршрутизации</span><span class="sxs-lookup"><span data-stu-id="5c6ac-134">Relevant Notifications for Stream Routing</span></span>](relevant-device-notifications-for-stream-routing.md)
-   [<span data-ttu-id="5c6ac-135">Рекомендации по реализации потоковой маршрутизации</span><span class="sxs-lookup"><span data-stu-id="5c6ac-135">Stream Routing Implementation Considerations</span></span>](stream-routing-implementation-considerations.md)

<span data-ttu-id="5c6ac-136">Следующие примеры, включенные в Windows SDK, демонстрируют, как приложение может управлять уведомлениями маршрутизации потоков.</span><span class="sxs-lookup"><span data-stu-id="5c6ac-136">The following samples, included in the Windows SDK, demonstrate how an application can handle stream routing notifications.</span></span>

-   [<span data-ttu-id="5c6ac-137">рендершаредтимердривен</span><span class="sxs-lookup"><span data-stu-id="5c6ac-137">RenderSharedTimerDriven</span></span>](rendersharedtimerdriven.md)
-   [<span data-ttu-id="5c6ac-138">рендершаредевентдривен</span><span class="sxs-lookup"><span data-stu-id="5c6ac-138">RenderSharedEventDriven</span></span>](rendersharedeventdriven.md)
-   [<span data-ttu-id="5c6ac-139">рендерексклусиветимердривен</span><span class="sxs-lookup"><span data-stu-id="5c6ac-139">RenderExclusiveTimerDriven</span></span>](renderexclusivetimerdriven.md)
-   [<span data-ttu-id="5c6ac-140">рендерексклусививентдривен</span><span class="sxs-lookup"><span data-stu-id="5c6ac-140">RenderExclusiveEventDriven</span></span>](renderexclusiveeventdriven.md)
-   [<span data-ttu-id="5c6ac-141">каптурешаредтимердривен</span><span class="sxs-lookup"><span data-stu-id="5c6ac-141">CaptureSharedTimerDriven</span></span>](capturesharedtimerdriven.md)
-   [<span data-ttu-id="5c6ac-142">каптурешаредевентдривен</span><span class="sxs-lookup"><span data-stu-id="5c6ac-142">CaptureSharedEventDriven</span></span>](capturesharedeventdriven.md)

## <a name="related-topics"></a><span data-ttu-id="5c6ac-143">См. также</span><span class="sxs-lookup"><span data-stu-id="5c6ac-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c6ac-144">Управление потоками</span><span class="sxs-lookup"><span data-stu-id="5c6ac-144">Stream Management</span></span>](stream-management.md)
</dt> <dt>

[<span data-ttu-id="5c6ac-145">Сведения об API Ммдевице</span><span class="sxs-lookup"><span data-stu-id="5c6ac-145">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="5c6ac-146">О ВАСАПИ</span><span class="sxs-lookup"><span data-stu-id="5c6ac-146">About WASAPI</span></span>](wasapi.md)
</dt> </dl>

 

 



