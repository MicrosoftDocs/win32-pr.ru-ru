---
description: Exclusive-Modeные потоки
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Exclusive-Modeные потоки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7722dd3463346e976f30a77949f56026a2425624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990573"
---
# <a name="exclusive-mode-streams"></a><span data-ttu-id="a9ec3-103">Exclusive-Modeные потоки</span><span class="sxs-lookup"><span data-stu-id="a9ec3-103">Exclusive-Mode Streams</span></span>

<span data-ttu-id="a9ec3-104">Как упоминалось ранее, если приложение открывает поток в монопольном режиме, приложение имеет эксклюзивное использование устройства конечной точки аудио, которое воспроизводит или записывает поток.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-104">As explained previously, if an application opens a stream in exclusive mode, the application has exclusive use of the audio endpoint device that plays or records the stream.</span></span> <span data-ttu-id="a9ec3-105">В отличие от этого, несколько приложений могут совместно использовать звуковое устройство для конечных точек, открывая потоки общего режима на устройстве.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-105">In contrast, several applications can share an audio endpoint device by opening shared-mode streams on the device.</span></span>

<span data-ttu-id="a9ec3-106">Доступ к звуковому устройству в монопольном режиме может блокировать критические системные звуки, предотвращать взаимодействие с другими приложениями и иным образом снизить удобство работы пользователя.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-106">Exclusive-mode access to an audio device can block crucial system sounds, prevent interoperability with other applications, and otherwise degrade the user experience.</span></span> <span data-ttu-id="a9ec3-107">Чтобы устранить эти проблемы, приложение с потоком в монопольном режиме обычно освобождает управление звуковым устройством, когда приложение не является основным процессом или не является активной потоковой передачей.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-107">To mitigate these problems, an application with an exclusive-mode stream typically relinquishes control of the audio device when the application is not the foreground process or is not actively streaming.</span></span>

<span data-ttu-id="a9ec3-108">Задержка потока — это задержка, которая связана с расположением данных, соединяющим буфер конечной точки приложения с устройством конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-108">Stream latency is the delay that is inherent in the data path that connects an application's endpoint buffer with an audio endpoint device.</span></span> <span data-ttu-id="a9ec3-109">Для потока отрисовки задержка — это максимальная задержка от времени, когда приложение записывает пример в буфер конечной точки до момента передачи образца через динамики.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-109">For a rendering stream, the latency is the maximum delay from the time that an application writes a sample to an endpoint buffer to the time that the sample is heard through the speakers.</span></span> <span data-ttu-id="a9ec3-110">Для потока записи задержка — это максимальная задержка от времени, когда звук попадает в микрофон, до момента, когда приложение может прочитать образец для этого звука из буфера конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-110">For a capture stream, the latency is the maximum delay from the time that a sound enters the microphone to the time that an application can read the sample for that sound from the endpoint buffer.</span></span>

<span data-ttu-id="a9ec3-111">Приложения, использующие потоки с монопольным режимом, часто делают это, так как они нуждаются в низких задержках между устройствами конечных точек аудио и потоками приложения, которые обращаются к буферам конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-111">Applications that use exclusive-mode streams often do so because they require low latencies in the data paths between the audio endpoint devices and the application threads that access the endpoint buffers.</span></span> <span data-ttu-id="a9ec3-112">Как правило, эти потоки работают с относительно высоким приоритетом и сами по себе запланируются на периодические интервалы, близкие к одному или тому же, что и период, который разделяет последовательную обработку, продающуюся звуковым оборудованием.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-112">Typically, these threads run at relatively high priority and schedule themselves to run at periodic intervals that are close to or the same as the periodic interval that separates successive processing passes by the audio hardware.</span></span> <span data-ttu-id="a9ec3-113">Во время каждого прохода звуковое оборудование обрабатывает новые данные в буферах конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-113">During each pass, the audio hardware processes the new data in the endpoint buffers.</span></span>

<span data-ttu-id="a9ec3-114">Для достижения наименьшей задержки потока приложению может потребоваться специальное звуковое оборудование и компьютерная система, которая будет легко загружена.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-114">To achieve the smallest stream latencies, an application might require both special audio hardware, and a computer system that is lightly loaded.</span></span> <span data-ttu-id="a9ec3-115">Появление звукового оборудования, превышающего ограничения по времени, или загрузка системы с конкурирующими задачами с высоким приоритетом может вызвать сбой в потоке звука с низкой задержкой.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-115">Driving the audio hardware beyond its timing limits or loading the system with competing high-priority tasks might cause a glitch in a low-latency audio stream.</span></span> <span data-ttu-id="a9ec3-116">Например, для потока отрисовки может произойти сбой, если приложению не удается выполнить запись в буфер конечной точки до того, как звуковая аппаратура прочитает буфер или если оборудование не сможет прочитать буфер до момента, когда буфер будет воспроизведен.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-116">For example, for a rendering stream, a glitch can occur if the application fails to write to an endpoint buffer before the audio hardware reads the buffer, or if the hardware fails to read the buffer before the time that the buffer is scheduled to play.</span></span> <span data-ttu-id="a9ec3-117">Как правило, приложение, предназначенное для работы на самых разнообразных звуковых устройствах и в широком диапазоне систем, должно ослабить свои требования к времени, чтобы избежать сбоев во всех целевых средах.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-117">Typically, an application that is intended to run on a wide variety of audio hardware and in a broad range of systems should relax its timing requirements enough to avoid glitches in all target environments.</span></span>

<span data-ttu-id="a9ec3-118">В Windows Vista предусмотрено несколько функций для поддержки приложений, требующих потоковых аудио с низкой задержкой.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-118">Windows Vista has several features to support applications that require low-latency audio streams.</span></span> <span data-ttu-id="a9ec3-119">Как обсуждалось в [пользовательских компонентах аудио](user-mode-audio-components.md), приложения, выполняющие критически важные для времени операции, могут вызывать функции службы управления правами (MMCSS) класса мультимедиа для повышения приоритета потоков без блокировки ресурсов ЦП на приложения с более низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-119">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), applications that perform time-critical operations can call the Multimedia Class Scheduler Service (MMCSS) functions to increase thread priority without denying CPU resources to lower-priority applications.</span></span> <span data-ttu-id="a9ec3-120">Кроме того, метод [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) поддерживает \_ флаг аудклнт стреамфлагс \_ вложенный EventCallback, позволяющий потоку обслуживания буфера приложения запланировать его выполнение, когда новый буфер станет доступен с звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-120">In addition, the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method supports an AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK flag that enables an application's buffer-servicing thread to schedule its execution to occur when a new buffer becomes available from the audio device.</span></span> <span data-ttu-id="a9ec3-121">Используя эти функции, поток приложения может уменьшить неопределенность при выполнении, что снижает риск возникновения сбоев в потоке звука с низкой задержкой.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-121">By using these features, an application thread can reduce uncertainty about when it will execute, thereby decreasing the risk of glitches in a low-latency audio stream.</span></span>

<span data-ttu-id="a9ec3-122">Драйверы старых звуковых адаптеров, скорее всего, используют интерфейс драйвера устройства Вавециклик или ВавепЦи (DDI), тогда как драйверы для новых звуковых адаптеров, скорее всего, будут поддерживать DDI Ваверт.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-122">The drivers for older audio adapters are likely to use the WaveCyclic or WavePci device driver interface (DDI), whereas the drivers for newer audio adapters are more likely to support the WaveRT DDI.</span></span> <span data-ttu-id="a9ec3-123">Для приложений с эксклюзивным режимом драйверы Ваверт могут обеспечить лучшую производительность, чем драйверы Вавециклик или ВавепЦи, но для драйверов Ваверт требуются дополнительные аппаратные возможности.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-123">For exclusive-mode applications, WaveRT drivers can provide better performance than WaveCyclic or WavePci drivers, but WaveRT drivers require additional hardware capabilities.</span></span> <span data-ttu-id="a9ec3-124">Эти возможности включают возможность совместного использования буферов оборудования непосредственно с приложениями.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-124">These capabilities include the ability to share hardware buffers directly with applications.</span></span> <span data-ttu-id="a9ec3-125">При непосредственном совместном использовании не требуется вмешательство системы для передачи данных между приложением с монопольным режимом и звуковым оборудованием.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-125">With direct sharing, no system intervention is required to transfer data between an exclusive-mode application and the audio hardware.</span></span> <span data-ttu-id="a9ec3-126">Драйверы Вавециклик и ВавепЦи подходят для старых и менее производительных звуковых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-126">In contrast, WaveCyclic and WavePci drivers are suitable for older, less capable audio adapters.</span></span> <span data-ttu-id="a9ec3-127">Эти адаптеры используют системное программное обеспечение для передачи блоков данных (подключенных к системным пакетам ввода-вывода и запросов IRP) между буферами приложений и аппаратными буферами.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-127">These adapters rely on system software to transport blocks of data (attached to system I/O request packets, or IRPs) between application buffers and hardware buffers.</span></span> <span data-ttu-id="a9ec3-128">Кроме того, устройства USB аудио используют системное по для передачи данных между буферами приложений и аппаратными буферами.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-128">In addition, USB audio devices rely on system software to transport data between application buffers and hardware buffers.</span></span> <span data-ttu-id="a9ec3-129">Чтобы повысить производительность приложений с монопольным режимом, подключающихся к звуковым устройствам, которые используют систему для передачи данных, ВАСАПИ автоматически повышает приоритет системных потоков, передающих данные между приложениями и оборудованием.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-129">To improve the performance of exclusive-mode applications that connect to audio devices that rely on the system for data transport, WASAPI automatically increases the priority of the system threads that transfer data between the applications and the hardware.</span></span> <span data-ttu-id="a9ec3-130">ВАСАПИ использует MMCSS для увеличения приоритета потока.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-130">WASAPI uses MMCSS to increase the thread priority.</span></span> <span data-ttu-id="a9ec3-131">В Windows Vista, если системный поток управляет транспортом данных для потока воспроизведения в монопольном режиме с форматом PCM и периодом устройства менее 10 миллисекунд, ВАСАПИ назначает имя задачи MMCSS "Pro Audio" потоку.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-131">In Windows Vista, if a system thread manages data transport for an exclusive-mode audio playback stream with a PCM format and a device period of less than 10 milliseconds, WASAPI assigns the MMCSS task name "Pro Audio" to the thread.</span></span> <span data-ttu-id="a9ec3-132">Если период устройства потока больше или равен 10 миллисекундам, ВАСАПИ присваивает потоку имя задачи MMCSS "Audio".</span><span class="sxs-lookup"><span data-stu-id="a9ec3-132">If the device period of the stream is greater than or equal to 10 milliseconds, WASAPI assigns the MMCSS task name "Audio" to the thread.</span></span> <span data-ttu-id="a9ec3-133">Дополнительные сведения о Вавециклик, ВавепЦи и Ваверт ДДИС см. в документации по Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-133">For more information about the WaveCyclic, WavePci, and WaveRT DDIs, see the Windows DDK documentation.</span></span> <span data-ttu-id="a9ec3-134">Сведения о выборе соответствующего периода устройства см. в разделе [**иаудиоклиент:: жетдевицепериод**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span><span class="sxs-lookup"><span data-stu-id="a9ec3-134">For information about selecting an appropriate device period, see [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span></span>

<span data-ttu-id="a9ec3-135">Как описано в разделе [элементы управления томами сеанса](session-volume-controls.md), [Васапи](wasapi.md) предоставляет интерфейсы [**исимплеаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**ичаннелаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)и [**иаудиостреамволуме**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) для управления уровнями громкости звуковых потоков в общем режиме.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-135">As described in [Session Volume Controls](session-volume-controls.md), [WASAPI](wasapi.md) provides the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces for controlling the volume levels of shared-mode audio streams.</span></span> <span data-ttu-id="a9ec3-136">Однако элементы управления в этих интерфейсах не влияют на потоки с монопольным режимом.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-136">However, the controls in these interfaces have no effect on exclusive-mode streams.</span></span> <span data-ttu-id="a9ec3-137">Вместо этого приложения, которые управляют потоками в монопольном режиме, обычно используют интерфейс [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) в [API ендпоинтволуме](endpointvolume-api.md) для управления уровнями громкости этих потоков.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-137">Instead, applications that manage exclusive-mode streams typically use the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the [EndpointVolume API](endpointvolume-api.md) to control the volume levels of those streams.</span></span> <span data-ttu-id="a9ec3-138">Сведения об этом интерфейсе см. в разделе [Управление томами конечных точек](endpoint-volume-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a9ec3-138">For information about this interface, see [Endpoint Volume Controls](endpoint-volume-controls.md).</span></span>

<span data-ttu-id="a9ec3-139">Для каждого устройства воспроизведения и устройства записи в системе пользователь может управлять возможностью использования устройства в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-139">For each playback device and capture device in the system, the user can control whether the device can be used in exclusive mode.</span></span> <span data-ttu-id="a9ec3-140">Если пользователь отключает использование устройства в монопольном режиме, устройство может использоваться для воспроизведения или записи только потоков в общем режиме.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-140">If the user disables exclusive-mode use of the device, the device can be used to play or record only shared-mode streams.</span></span>

<span data-ttu-id="a9ec3-141">Если пользователь разрешает использовать устройство в монопольном режиме, он также может управлять тем, будет ли запрос приложением использовать устройство в монопольном режиме, чтобы использовать его в приложениях, которые могут в настоящее время воспроизводить или записывать потоки общего режима через устройство.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-141">If the user enables exclusive-mode use of the device, the user can also control whether a request by an application to use the device in exclusive mode will preempt the use of the device by applications that might currently be playing or recording shared-mode streams through the device.</span></span> <span data-ttu-id="a9ec3-142">Если вызываемое прерывание включено, запрос приложения, чтобы получить монопольный контроль над устройством, будет успешным, если устройство в данный момент не используется или устройство используется в общем режиме, но запрос завершается сбоем, если другое приложение уже имеет монопольный контроль над устройством.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-142">If preemption is enabled, a request by an application to take exclusive control of the device succeeds if the device is currently not in use, or if the device is being used in shared mode, but the request fails if another application already has exclusive control of the device.</span></span> <span data-ttu-id="a9ec3-143">Если прерывание отключено, запрос приложения на монопольное управление устройством завершается успешно, если устройство в настоящее время не используется, но запрос завершается неудачей, если устройство уже используется в режиме общего доступа или в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-143">If preemption is disabled, a request by an application to take exclusive control of the device succeeds if the device is not currently in use, but the request fails if the device is already being used either in shared mode or in exclusive mode.</span></span>

<span data-ttu-id="a9ec3-144">В Windows Vista параметры по умолчанию для устройства конечной точки аудио приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-144">In Windows Vista, the default settings for an audio endpoint device are the following:</span></span>

-   <span data-ttu-id="a9ec3-145">Устройство можно использовать для воспроизведения или записи потоков с монопольным режимом.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-145">The device can be used to play or record exclusive-mode streams.</span></span>
-   <span data-ttu-id="a9ec3-146">Запрос на использование устройства для воспроизведения или записи потока с монопольным режимом вызывает перегрузку любого потока общего режима, который в данный момент воспроизводится или записывается на устройстве.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-146">A request to use a device to play or record an exclusive-mode stream preempts any shared-mode stream that is currently being played or recorded through the device.</span></span>

<span data-ttu-id="a9ec3-147">**Изменение параметров монопольного режима для устройства воспроизведения или записи**</span><span class="sxs-lookup"><span data-stu-id="a9ec3-147">**To change the exclusive-mode settings of a playback or recording device**</span></span>

1.  <span data-ttu-id="a9ec3-148">Щелкните правой кнопкой мыши значок динамика в области уведомлений, расположенном в правой части панели задач, и выберите пункт **устройства воспроизведения** или **записывающие устройства**.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-148">Right-click the speaker icon in the notification area, which is located on the right side of the taskbar, and select **Playback Devices** or **Recording Devices**.</span></span> <span data-ttu-id="a9ec3-149">(В качестве альтернативы запустите Панель управления Windows Mmsys.cpl из окна командной строки.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-149">(As an alternative, run the Windows multimedia control panel, Mmsys.cpl, from a Command Prompt window.</span></span> <span data-ttu-id="a9ec3-150">Дополнительные сведения см. в разделе Примечания [в \_ \_ константах в состоянии устройства XXX](device-state-xxx-constants.md).)</span><span class="sxs-lookup"><span data-stu-id="a9ec3-150">For more information, see Remarks in [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).)</span></span>
2.  <span data-ttu-id="a9ec3-151">После появления **звукового** окна выберите **Воспроизведение** или **запись**.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-151">After the **Sound** window appears, select **Playback** or **Recording**.</span></span> <span data-ttu-id="a9ec3-152">Затем выберите запись в списке имен устройств и нажмите кнопку **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-152">Next, select an entry in the list of device names, and click **Properties**.</span></span>
3.  <span data-ttu-id="a9ec3-153">После появления окна **Свойства** нажмите кнопку **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-153">After the **Properties** window appears, click **Advanced**.</span></span>
4.  <span data-ttu-id="a9ec3-154">Чтобы разрешить приложениям использовать устройство в монопольном режиме, установите флажок **Разрешить приложениям принимать монопольный контроль над этим устройством**.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-154">To enable applications to use the device in exclusive mode, check the box labeled **Allow applications to take exclusive control of this device**.</span></span> <span data-ttu-id="a9ec3-155">Чтобы отключить использование устройства в монопольном режиме, снимите флажок.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-155">To disable exclusive-mode use of the device, clear the check box.</span></span>
5.  <span data-ttu-id="a9ec3-156">Если включено использование устройства в монопольном режиме, можно указать, будет ли запрос на монопольный доступ к этому устройству выполняться, если устройство воспроизводит или записывает потоки в общем режиме.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-156">If exclusive-mode use of the device is enabled, you can specify whether a request for exclusive control of the device will succeed if the device is currently playing or recording shared-mode streams.</span></span> <span data-ttu-id="a9ec3-157">Чтобы предоставить приложениям с монопольным режимом приоритет над приложениями в общем режиме, установите флажок **задать приоритет для приложений с монопольным** режимом.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-157">To give exclusive-mode applications priority over shared-mode applications, check the box labeled **Give exclusive mode applications priority**.</span></span> <span data-ttu-id="a9ec3-158">Чтобы запретить приложениям с монопольным режимом приоритетно использовать приложения общего режима, снимите флажок.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-158">To deny exclusive-mode applications priority over shared-mode applications, clear the check box.</span></span>

<span data-ttu-id="a9ec3-159">В следующем примере кода показано, как воспроизвести аудиопоток с низкой задержкой на устройстве рендеринга звука, настроенном для использования в монопольном режиме:</span><span class="sxs-lookup"><span data-stu-id="a9ec3-159">The following code example shows how to play a low-latency audio stream on an audio-rendering device that is configured for use in exclusive mode:</span></span>


```C++
//-----------------------------------------------------------
// Play an exclusive-mode stream on the default audio
// rendering device. The PlayExclusiveStream function uses
// event-driven buffering and MMCSS to play the stream at
// the minimum latency supported by the device.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayExclusiveStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = 0;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    HANDLE hEvent = NULL;
    HANDLE hTask = NULL;
    UINT32 bufferFrameCount;
    BYTE *pData;
    DWORD flags = 0;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    // Call a helper function to negotiate with the audio
    // device for an exclusive-mode stream format.
    hr = GetStreamFormat(pAudioClient, &pwfx);
    EXIT_ON_ERROR(hr)

    // Initialize the stream to play at the minimum latency.
    hr = pAudioClient->GetDevicePeriod(NULL, &hnsRequestedDuration);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_EXCLUSIVE,
                         AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
                         hnsRequestedDuration,
                         hnsRequestedDuration,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Create an event handle and register it for
    // buffer-event notifications.
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = E_FAIL;
        goto Exit;
    }

    hr = pAudioClient->SetEventHandle(hEvent);
    EXIT_ON_ERROR(hr);

    // Get the actual size of the two allocated buffers.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // To reduce latency, load the first buffer with data
    // from the audio source before starting the stream.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Ask MMCSS to temporarily boost the thread priority
    // to reduce glitches while the low-latency stream plays.
    DWORD taskIndex = 0;
    hTask = AvSetMmThreadCharacteristics(TEXT("Pro Audio"), &taskIndex);
    if (hTask == NULL)
    {
        hr = E_FAIL;
        EXIT_ON_ERROR(hr)
    }

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills one of the two buffers.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Wait for next buffer event to be signaled.
        DWORD retval = WaitForSingleObject(hEvent, 2000);
        if (retval != WAIT_OBJECT_0)
        {
            // Event handle timed out after a 2-second wait.
            pAudioClient->Stop();
            hr = ERROR_TIMEOUT;
            goto Exit;
        }

        // Grab the next empty buffer from the audio device.
        hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
        EXIT_ON_ERROR(hr)

        // Load the buffer with data from the audio source.
        hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for the last buffer to play before stopping.
    Sleep((DWORD)(hnsRequestedDuration/REFTIMES_PER_MILLISEC));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    if (hEvent != NULL)
    {
        CloseHandle(hEvent);
    }
    if (hTask != NULL)
    {
        AvRevertMmThreadCharacteristics(hTask);
    }
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



<span data-ttu-id="a9ec3-160">В предыдущем примере кода функция Плайексклусивестреам выполняется в потоке приложения, который выполняет обслуживание буферов конечной точки во время воспроизведения потока отрисовки.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-160">In the preceding code example, the PlayExclusiveStream function runs in the application thread that services the endpoint buffers while a rendering stream is playing.</span></span> <span data-ttu-id="a9ec3-161">Функция принимает один параметр Пмисаурце, который является указателем на объект, принадлежащий определяемому клиентом классу Мяудиосаурце.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-161">The function takes a single parameter, pMySource, which is a pointer to an object that belongs to a client-defined class, MyAudioSource.</span></span> <span data-ttu-id="a9ec3-162">Этот класс содержит две функции члена, LoadData и Сетформат, которые вызываются в примере кода.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-162">This class has two member functions, LoadData and SetFormat, that are called in the code example.</span></span> <span data-ttu-id="a9ec3-163">Мяудиосаурце описывается в разделе [Подготовка потока](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="a9ec3-163">MyAudioSource is described in [Rendering a Stream](rendering-a-stream.md).</span></span>

<span data-ttu-id="a9ec3-164">Функция Плайексклусивестреам вызывает вспомогательную функцию Жетстреамформат, которая согласовывается с устройством отрисовки по умолчанию, чтобы определить, поддерживает ли устройство формат потока с монопольным режимом, который подходит для использования приложением.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-164">The PlayExclusiveStream function calls a helper function, GetStreamFormat, that negotiates with the default rendering device to determine whether the device supports an exclusive-mode stream format that is suitable for use by the application.</span></span> <span data-ttu-id="a9ec3-165">Код функции Жетстреамформат не отображается в примере кода. Это связано с тем, что сведения о его реализации полностью зависят от требований приложения.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-165">The code for the GetStreamFormat function does not appear in the code example; that is because the details of its implementation depend entirely on the requirements of the application.</span></span> <span data-ttu-id="a9ec3-166">Однако операцию функции Жетстреамформат можно описать просто — она вызывает метод [**иаудиоклиент:: исформатсуппортед**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) один или несколько раз, чтобы определить, поддерживает ли устройство подходящий формат.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-166">However, the operation of the GetStreamFormat function can be described simply—it calls the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method one or more times to determine whether the device supports a suitable format.</span></span> <span data-ttu-id="a9ec3-167">Требования приложения определяют, какие форматы Жетстреамформат представляют методу **исформатсуппортед** , и порядок их представления.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-167">The requirements of the application dictate which formats GetStreamFormat presents to the **IsFormatSupported** method and the order in which it presents them.</span></span> <span data-ttu-id="a9ec3-168">Дополнительные сведения о **исформатсуппортед** см. в разделе [форматы устройств](device-formats.md).</span><span class="sxs-lookup"><span data-stu-id="a9ec3-168">For more information about **IsFormatSupported**, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="a9ec3-169">После вызова Жетстреамформат функция Плайексклусивестреам вызывает метод [**иаудиоклиент:: жетдевицепериод**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) , чтобы получить минимальный период устройства, поддерживаемый звуковым оборудованием.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-169">After the GetStreamFormat call, the PlayExclusiveStream function calls the [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) method to obtain the minimum device period supported by the audio hardware.</span></span> <span data-ttu-id="a9ec3-170">Затем функция вызывает метод [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) для запроса длительности буфера равным минимальному периоду.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-170">Next, the function calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method to request a buffer duration equal to the minimum period.</span></span> <span data-ttu-id="a9ec3-171">Если вызов будет выполнен, метод **Initialize** выделяет два буфера конечной точки, каждая из которых равна минимальному периоду.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-171">If the call succeeds, the **Initialize** method allocates two endpoint buffers, each of which is equal in duration to the minimum period.</span></span> <span data-ttu-id="a9ec3-172">Позднее, когда начнется запуск аудиопотока, приложение и звуковое оборудование будут совместно использовать два буфера в «пинг-теннисе», т. е. когда приложение записывает данные в один буфер, оборудование считывает данные из другого буфера.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-172">Later, when the audio stream begins running, the application and audio hardware will share the two buffers in "ping-pong" fashion—that is, while the application writes to one buffer, the hardware reads from the other buffer.</span></span>

<span data-ttu-id="a9ec3-173">Перед запуском потока функция Плайексклусивестреам выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a9ec3-173">Before starting the stream, the PlayExclusiveStream function does the following:</span></span>

-   <span data-ttu-id="a9ec3-174">Создает и регистрирует обработчик событий, через который он будет получать уведомления о готовности буферов к заполнению.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-174">Creates and registers the event handle through which it will receive notifications when buffers become ready to fill.</span></span>
-   <span data-ttu-id="a9ec3-175">Заполняет первый буфер данными из источника аудио, чтобы уменьшить задержку, с которой начнется выполнение потока при проходе первоначального звукового сигнала.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-175">Fills the first buffer with data from the audio source to reduce the delay from when the stream starts running to when the initial sound is heard.</span></span>
-   <span data-ttu-id="a9ec3-176">Вызывает функцию **авсетммсреадчарактеристикс** , чтобы запросить, что служба MMCSS повышает приоритет потока, в котором выполняется плайексклусивестреам.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-176">Calls the **AvSetMmThreadCharacteristics** function to request that MMCSS increase the priority of the thread in which PlayExclusiveStream executes.</span></span> <span data-ttu-id="a9ec3-177">(Когда поток прекращает выполнение, вызов функции **авревертммсреадчарактеристикс** восстанавливает исходный приоритет потока.)</span><span class="sxs-lookup"><span data-stu-id="a9ec3-177">(When the stream stops running, the **AvRevertMmThreadCharacteristics** function call restores the original thread priority.)</span></span>

<span data-ttu-id="a9ec3-178">Дополнительные сведения о **авсетммсреадчарактеристикс** и **авревертммсреадчарактеристикс** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-178">For more information about **AvSetMmThreadCharacteristics** and **AvRevertMmThreadCharacteristics**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="a9ec3-179">Во время выполнения потока каждая итерация цикла **while** в предыдущем примере кода заполняет один буфер конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-179">While the stream is running, each iteration of the **while**-loop in the preceding code example fills one endpoint buffer.</span></span> <span data-ttu-id="a9ec3-180">Между итерациями вызов функции **WaitForSingleObject** ожидает получения сигнала для дескриптора события.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-180">Between iterations, the **WaitForSingleObject** function call waits for the event handle to be signaled.</span></span> <span data-ttu-id="a9ec3-181">Когда дескриптор получает сигнал, тело цикла выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a9ec3-181">When the handle is signaled, the loop body does the following:</span></span>

1.  <span data-ttu-id="a9ec3-182">Вызывает метод [**иаудиорендерклиент::**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) GetNext для получения следующего буфера.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-182">Calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method to get the next buffer.</span></span>
2.  <span data-ttu-id="a9ec3-183">Заполняет буфер.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-183">Fills the buffer.</span></span>
3.  <span data-ttu-id="a9ec3-184">Вызывает метод [**иаудиорендерклиент:: релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , чтобы освободить буфер.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-184">Calls the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method to release the buffer.</span></span>

<span data-ttu-id="a9ec3-185">Дополнительные сведения о **WaitForSingleObject** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-185">For more information about **WaitForSingleObject**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="a9ec3-186">Если звуковой адаптер управляется драйвером Ваверт, сигнал дескриптора события привязывается к уведомлениям передачи DMA с аудио-оборудования.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-186">If the audio adapter is controlled by a WaveRT driver, the signaling of the event handle is tied to the DMA-transfer notifications from the audio hardware.</span></span> <span data-ttu-id="a9ec3-187">Для звукового устройства USB или для звукового устройства, управляемого драйвером Вавециклик или ВавепЦи, сигнал дескриптора события связан с завершением запросов IRP, которые передают данные из буфера приложения в аппаратный буфер.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-187">For a USB audio device, or for an audio device that is controlled by a WaveCyclic or WavePci driver, the signaling of the event handle is tied to completions of the IRPs that transfer data from the application buffer to the hardware buffer.</span></span>

<span data-ttu-id="a9ec3-188">Предыдущий пример кода передает звуковое оборудование и компьютерную систему на свои ограничения производительности.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-188">The preceding code example pushes the audio hardware and the computer system to their performance limits.</span></span> <span data-ttu-id="a9ec3-189">Во-первых, чтобы сократить задержку потока, приложение планирует поток обслуживания буферов для использования минимального периода, поддерживаемого звуковым оборудованием.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-189">First, to reduce the stream latency, the application schedules its buffer-servicing thread to use the minimum device period that the audio hardware will support.</span></span> <span data-ttu-id="a9ec3-190">Во-вторых, чтобы обеспечить надежное выполнение потока в каждом из периодов устройства, вызов функции **авсетммсреадчарактеристикс** устанавливает для параметра имя_задания значение "Pro Audio", т. е. в Windows Vista имя задачи по умолчанию с наивысшим приоритетом.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-190">Second, to ensure that the thread reliably executes within each device period, the **AvSetMmThreadCharacteristics** function call sets the TaskName parameter to "Pro Audio", which is, in Windows Vista, the default task name with the highest priority.</span></span> <span data-ttu-id="a9ec3-191">Определите, могут ли требования к времени приложения быть неослабленными без ущерба для его полезности.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-191">Consider whether the timing requirements of your application might be relaxed without compromising its usefulness.</span></span> <span data-ttu-id="a9ec3-192">Например, приложение может запланировать использование потока обслуживания буферов в течение периода, превышающего минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-192">For example, the application might schedule its buffer-servicing thread to use a period that is longer than the minimum.</span></span> <span data-ttu-id="a9ec3-193">Более длительный период может безопасно разрешать использование более низкого приоритета потока.</span><span class="sxs-lookup"><span data-stu-id="a9ec3-193">A longer period might safely allow the use of a lower thread priority.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9ec3-194">См. также</span><span class="sxs-lookup"><span data-stu-id="a9ec3-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9ec3-195">Управление потоками</span><span class="sxs-lookup"><span data-stu-id="a9ec3-195">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 



