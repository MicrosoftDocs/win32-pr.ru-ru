---
description: Управление потоками
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Управление потоками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07180d8b46f4d079c08f4b619cf4a7773a6104d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141851"
---
# <a name="stream-management"></a><span data-ttu-id="d22c4-103">Управление потоками</span><span class="sxs-lookup"><span data-stu-id="d22c4-103">Stream Management</span></span>

<span data-ttu-id="d22c4-104">После перечисления [устройств конечных точек аудио](audio-endpoint-devices.md) в системе и определения подходящего устройства для отрисовки или записи, следующая задача для клиентского приложения будет открывать подключение к оконечному устройству и управлять потоком звуковых данных по этому соединению.</span><span class="sxs-lookup"><span data-stu-id="d22c4-104">After enumerating the [audio endpoint devices](audio-endpoint-devices.md) in the system and identifying a suitable rendering or capture device, the next task for an audio client application is to open a connection with the endpoint device and to manage the flow of audio data over that connection.</span></span> <span data-ttu-id="d22c4-105">[Васапи](wasapi.md) позволяет клиентам создавать звуковые потоки и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="d22c4-105">[WASAPI](wasapi.md) enables clients to create and manage audio streams.</span></span>

<span data-ttu-id="d22c4-106">ВАСАПИ реализует несколько интерфейсов для предоставления службам управления потоками аудио клиентам.</span><span class="sxs-lookup"><span data-stu-id="d22c4-106">WASAPI implements several interfaces to provide stream-management services to audio clients.</span></span> <span data-ttu-id="d22c4-107">Основным интерфейсом является [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span><span class="sxs-lookup"><span data-stu-id="d22c4-107">The primary interface is [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span></span> <span data-ttu-id="d22c4-108">Клиент получает интерфейс **иаудиоклиент** для устройства конечной точки аудио, вызывая метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (с параметром *IID* которого задано значение **рефиид** IID \_ иаудиоклиент) для объекта Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d22c4-108">A client obtains the **IAudioClient** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioClient) on the endpoint object.</span></span>

<span data-ttu-id="d22c4-109">Клиент вызывает методы в интерфейсе [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="d22c4-109">The client calls the methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to do the following:</span></span>

-   <span data-ttu-id="d22c4-110">Узнайте, какие аудио форматы поддерживает устройство конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d22c4-110">Discover which audio formats the endpoint device supports.</span></span>
-   <span data-ttu-id="d22c4-111">Возвращает размер буфера конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d22c4-111">Get the endpoint buffer size.</span></span>
-   <span data-ttu-id="d22c4-112">Получение формата потока и задержки.</span><span class="sxs-lookup"><span data-stu-id="d22c4-112">Get the stream format and latency.</span></span>
-   <span data-ttu-id="d22c4-113">Запускает, останавливает и сбрасывает поток, который проходит через устройство конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d22c4-113">Start, stop, and reset the stream that flows through the endpoint device.</span></span>
-   <span data-ttu-id="d22c4-114">Доступ к дополнительным службам аудио.</span><span class="sxs-lookup"><span data-stu-id="d22c4-114">Access additional audio services.</span></span>

<span data-ttu-id="d22c4-115">Чтобы создать поток, клиент вызывает метод [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="d22c4-115">To create a stream, a client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="d22c4-116">С помощью этого метода клиент указывает формат данных для потока, размер буфера конечной точки и то, работает ли поток в общем или монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="d22c4-116">Through this method, the client specifies the data format for the stream, the size of the endpoint buffer, and whether the stream operates in shared or exclusive mode.</span></span>

<span data-ttu-id="d22c4-117">Остальные методы в интерфейсе [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) делятся на две группы:</span><span class="sxs-lookup"><span data-stu-id="d22c4-117">The remaining methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface fall into two groups:</span></span>

-   <span data-ttu-id="d22c4-118">Методы, которые могут вызываться только после открытия потока с помощью [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="d22c4-118">Methods that can be called only after the stream has been opened by [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="d22c4-119">Методы, которые могут быть вызваны в любое время до или после вызова [**инициализации**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="d22c4-119">Methods that can be called at any time before or after the [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call.</span></span>

<span data-ttu-id="d22c4-120">Следующие методы можно вызывать только после вызова [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):</span><span class="sxs-lookup"><span data-stu-id="d22c4-120">The following methods can be called only after the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):</span></span>

-   [<span data-ttu-id="d22c4-121">**Иаудиоклиент:: Жетбуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="d22c4-121">**IAudioClient::GetBufferSize**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [<span data-ttu-id="d22c4-122">**Иаудиоклиент:: Жеткуррентпаддинг**</span><span class="sxs-lookup"><span data-stu-id="d22c4-122">**IAudioClient::GetCurrentPadding**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [<span data-ttu-id="d22c4-123">**Иаудиоклиент:: "Услуга"**</span><span class="sxs-lookup"><span data-stu-id="d22c4-123">**IAudioClient::GetService**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [<span data-ttu-id="d22c4-124">**Иаудиоклиент:: Жетстреамлатенци**</span><span class="sxs-lookup"><span data-stu-id="d22c4-124">**IAudioClient::GetStreamLatency**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [<span data-ttu-id="d22c4-125">**Иаудиоклиент:: Reset**</span><span class="sxs-lookup"><span data-stu-id="d22c4-125">**IAudioClient::Reset**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [<span data-ttu-id="d22c4-126">**Иаудиоклиент:: Start**</span><span class="sxs-lookup"><span data-stu-id="d22c4-126">**IAudioClient::Start**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [<span data-ttu-id="d22c4-127">**Иаудиоклиент:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="d22c4-127">**IAudioClient::Stop**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

<span data-ttu-id="d22c4-128">Следующие методы можно вызывать до или после вызова [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) :</span><span class="sxs-lookup"><span data-stu-id="d22c4-128">The following methods can be called before or after the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call:</span></span>

-   [<span data-ttu-id="d22c4-129">**Иаудиоклиент:: Жетдевицепериод**</span><span class="sxs-lookup"><span data-stu-id="d22c4-129">**IAudioClient::GetDevicePeriod**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [<span data-ttu-id="d22c4-130">**Иаудиоклиент:: Жетмиксформат**</span><span class="sxs-lookup"><span data-stu-id="d22c4-130">**IAudioClient::GetMixFormat**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [<span data-ttu-id="d22c4-131">**Иаудиоклиент:: Исформатсуппортед**</span><span class="sxs-lookup"><span data-stu-id="d22c4-131">**IAudioClient::IsFormatSupported**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

<span data-ttu-id="d22c4-132">Для доступа к дополнительным службам аудио клиента клиент вызывает метод [**иаудиоклиент::**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="d22c4-132">To access the additional audio client services, the client calls the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="d22c4-133">С помощью этого метода клиент может получить ссылки на следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="d22c4-133">Through this method, the client can obtain references to the following interfaces:</span></span>

-   [<span data-ttu-id="d22c4-134">**иаудиорендерклиент**</span><span class="sxs-lookup"><span data-stu-id="d22c4-134">**IAudioRenderClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    <span data-ttu-id="d22c4-135">Записывает данные отрисовки в буфер конечной точки отрисовки звука.</span><span class="sxs-lookup"><span data-stu-id="d22c4-135">Writes rendering data to an audio-rendering endpoint buffer.</span></span>

-   [<span data-ttu-id="d22c4-136">**иаудиокаптуреклиент**</span><span class="sxs-lookup"><span data-stu-id="d22c4-136">**IAudioCaptureClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    <span data-ttu-id="d22c4-137">Считывает записанные данные из буфера конечной точки записи звука.</span><span class="sxs-lookup"><span data-stu-id="d22c4-137">Reads captured data from an audio-capture endpoint buffer.</span></span>

-   [<span data-ttu-id="d22c4-138">**иаудиосессионконтрол**</span><span class="sxs-lookup"><span data-stu-id="d22c4-138">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    <span data-ttu-id="d22c4-139">Взаимодействует с диспетчером сеансов аудио для настройки и управления сеансом звука, связанным с потоком.</span><span class="sxs-lookup"><span data-stu-id="d22c4-139">Communicates with the audio session manager to configure and manage the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="d22c4-140">**исимплеаудиоволуме**</span><span class="sxs-lookup"><span data-stu-id="d22c4-140">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    <span data-ttu-id="d22c4-141">Управляет уровнем громкости звукового сеанса, связанного с потоком.</span><span class="sxs-lookup"><span data-stu-id="d22c4-141">Controls the volume level of the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="d22c4-142">**ичаннелаудиоволуме**</span><span class="sxs-lookup"><span data-stu-id="d22c4-142">**IChannelAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    <span data-ttu-id="d22c4-143">Управляет уровнями громкости отдельных каналов в сеансе звука, который связан с потоком.</span><span class="sxs-lookup"><span data-stu-id="d22c4-143">Controls the volume levels of the individual channels in the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="d22c4-144">**иаудиоклокк**</span><span class="sxs-lookup"><span data-stu-id="d22c4-144">**IAudioClock**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    <span data-ttu-id="d22c4-145">Отслеживает скорость потоковых данных и расположение потока.</span><span class="sxs-lookup"><span data-stu-id="d22c4-145">Monitors the stream data rate and stream position.</span></span>

<span data-ttu-id="d22c4-146">Кроме того, клиенты ВАСАПИ, которым требуется уведомление о событиях, связанных с сеансом, должны реализовать следующий интерфейс:</span><span class="sxs-lookup"><span data-stu-id="d22c4-146">In addition, WASAPI clients that require notification of session-related events should implement the following interface:</span></span>

-   [<span data-ttu-id="d22c4-147">**иаудиосессионевентс**</span><span class="sxs-lookup"><span data-stu-id="d22c4-147">**IAudioSessionEvents**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    <span data-ttu-id="d22c4-148">Чтобы получать уведомления о событиях, клиент передает указатель на интерфейс [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) в метод [**Иаудиосессионконтрол:: регистераудиосессионнотификатион**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) в качестве параметра вызова.</span><span class="sxs-lookup"><span data-stu-id="d22c4-148">To receive event notifications, the client passes a pointer to its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method as a call parameter.</span></span>

<span data-ttu-id="d22c4-149">Наконец, клиент может использовать API более высокого уровня для создания звукового потока, но также требует доступа к элементам управления сеанса и элементам управления громкостью для сеанса, содержащего поток.</span><span class="sxs-lookup"><span data-stu-id="d22c4-149">Finally, a client might use a higher-level API to create an audio stream, but also require access to the session controls and volume controls for the session that contains the stream.</span></span> <span data-ttu-id="d22c4-150">Интерфейс API более высокого уровня обычно не предоставляет такой доступ.</span><span class="sxs-lookup"><span data-stu-id="d22c4-150">A higher-level API typically does not provide this access.</span></span> <span data-ttu-id="d22c4-151">Клиент может получать элементы управления для определенного сеанса через интерфейс [**иаудиосессионманажер**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) .</span><span class="sxs-lookup"><span data-stu-id="d22c4-151">The client can obtain the controls for a particular session through the [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface.</span></span> <span data-ttu-id="d22c4-152">Этот интерфейс позволяет клиенту получать интерфейсы [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) и [**исимплеаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) для сеанса, не требуя от клиента использования интерфейса [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) для создания потока и назначения потока сеансу.</span><span class="sxs-lookup"><span data-stu-id="d22c4-152">This interface enables the client to obtain the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) and [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interfaces for a session without requiring the client to use the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to create a stream and to assign the stream to the session.</span></span> <span data-ttu-id="d22c4-153">Клиент получает интерфейс **иаудиосессионманажер** для устройства конечной точки аудио, вызывая метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (с параметром *IID* которого задано значение **рефиид** IID \_ иаудиосессионманажер) для объекта Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d22c4-153">A client obtains the **IAudioSessionManager** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioSessionManager) on the endpoint object.</span></span>

<span data-ttu-id="d22c4-154">Интерфейсы [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)и [**Иаудиосессионманажер**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) определены в файле заголовка аудиополици. h.</span><span class="sxs-lookup"><span data-stu-id="d22c4-154">The [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents), and [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interfaces are defined in header file Audiopolicy.h.</span></span> <span data-ttu-id="d22c4-155">Все остальные интерфейсы ВАСАПИ определены в файле заголовка Аудиоклиент. h.</span><span class="sxs-lookup"><span data-stu-id="d22c4-155">All other WASAPI interfaces are defined in header file Audioclient.h.</span></span>

<span data-ttu-id="d22c4-156">В следующих разделах описывается использование ВАСАПИ для управления звуковыми потоками.</span><span class="sxs-lookup"><span data-stu-id="d22c4-156">The following sections describe how to use WASAPI to manage audio streams:</span></span>

-   [<span data-ttu-id="d22c4-157">О ВАСАПИ</span><span class="sxs-lookup"><span data-stu-id="d22c4-157">About WASAPI</span></span>](wasapi.md)
-   [<span data-ttu-id="d22c4-158">Отрисовка потока</span><span class="sxs-lookup"><span data-stu-id="d22c4-158">Rendering a Stream</span></span>](rendering-a-stream.md)
-   [<span data-ttu-id="d22c4-159">Запись потока</span><span class="sxs-lookup"><span data-stu-id="d22c4-159">Capturing a Stream</span></span>](capturing-a-stream.md)
-   [<span data-ttu-id="d22c4-160">Запись замыкания на себя</span><span class="sxs-lookup"><span data-stu-id="d22c4-160">Loopback Recording</span></span>](loopback-recording.md)
-   [<span data-ttu-id="d22c4-161">Потоки с монопольным режимом</span><span class="sxs-lookup"><span data-stu-id="d22c4-161">Exclusive-Mode Streams</span></span>](exclusive-mode-streams.md)
-   [<span data-ttu-id="d22c4-162">Восстановление после ошибки Invalid-Device</span><span class="sxs-lookup"><span data-stu-id="d22c4-162">Recovering from an Invalid-Device Error</span></span>](recovering-from-an-invalid-device-error.md)
-   [<span data-ttu-id="d22c4-163">Использование коммуникационного устройства</span><span class="sxs-lookup"><span data-stu-id="d22c4-163">Using a Communication Device</span></span>](using-the-communication-device.md)
-   [<span data-ttu-id="d22c4-164">Потоковая маршрутизация</span><span class="sxs-lookup"><span data-stu-id="d22c4-164">Stream Routing</span></span>](stream-routing.md)

## <a name="related-topics"></a><span data-ttu-id="d22c4-165">См. также</span><span class="sxs-lookup"><span data-stu-id="d22c4-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d22c4-166">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="d22c4-166">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



