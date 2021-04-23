---
title: Отправка данных ASF в точку публикации
description: Отправка данных ASF в точку публикации
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- Пакет SDK для Windows Media Format, отправка данных ASF
- Пакет SDK для формата Windows Media, точки публикации
- Расширенный системный формат (ASF), отправка данных
- ASF (Расширенный системный формат), отправка данных
- Расширенный системный формат (ASF), точки публикации
- ASF (Расширенный системный формат), точки публикации
- точки публикации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f38f4d24a458681c4b0dc4ee6d1a73563bdd2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789241"
---
# <a name="sending-asf-data-to-a-publishing-point"></a><span data-ttu-id="c1c83-110">Отправка данных ASF в точку публикации</span><span class="sxs-lookup"><span data-stu-id="c1c83-110">Sending ASF Data to a Publishing Point</span></span>

<span data-ttu-id="c1c83-111">Пакет Windows Media Format SDK можно использовать для отправки данных ASF в точку публикации на сервере Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c1c83-111">You can use the Windows Media Format SDK to push ASF data to a publishing point on a Windows Media server.</span></span> <span data-ttu-id="c1c83-112">Затем сервер передает данные из этой точки публикации.</span><span class="sxs-lookup"><span data-stu-id="c1c83-112">The server then broadcasts the data from that publishing point.</span></span> <span data-ttu-id="c1c83-113">Этот сценарий полезен при записи или повторном кодировании содержимого на одном компьютере и необходимости распространения содержимого с другого компьютера (или нескольких компьютеров).</span><span class="sxs-lookup"><span data-stu-id="c1c83-113">This scenario is useful if you are capturing or re-encoding content on one computer, and wish to distribute the content from another computer (or several computers).</span></span> <span data-ttu-id="c1c83-114">Это также полезно, если необходимо переместить содержимое с компьютера в брандмауэре на сервер Windows Media, находящийся за пределами брандмауэра, так как для распространения push-уведомлений используется протокол HTTP.</span><span class="sxs-lookup"><span data-stu-id="c1c83-114">It is also useful if you need to move content from a computer inside a firewall to a Windows Media server outside the firewall, because push distribution uses the HTTP protocol.</span></span>

> [!Note]  
> <span data-ttu-id="c1c83-115">*Точка публикации* действует по сути как перенаправитель.</span><span class="sxs-lookup"><span data-stu-id="c1c83-115">A *publishing point* acts essentially like a redirector.</span></span> <span data-ttu-id="c1c83-116">Клиент указывает точку публикации в URL-адресе (например, mms://MyServer/MyPublishingPoint), и сервер преобразует это в запрос содержимого.</span><span class="sxs-lookup"><span data-stu-id="c1c83-116">The client specifies the publishing point in the URL (for example, mms://MyServer/MyPublishingPoint) and the server translates this into a request for content.</span></span>

 

<span data-ttu-id="c1c83-117">Чтобы отправить данные в точку публикации, присоедините объект приемника push-уведомлений к объекту модуля записи.</span><span class="sxs-lookup"><span data-stu-id="c1c83-117">To push data to the publishing point, attach the push sink object to the writer object.</span></span> <span data-ttu-id="c1c83-118">Приемник push-уведомлений используется для открытия подключения к серверу и управления сеансом принудительной отправки.</span><span class="sxs-lookup"><span data-stu-id="c1c83-118">The push sink is used to open the connection to the server and manage the push session.</span></span> <span data-ttu-id="c1c83-119">Объект модуля записи обрабатывает все остальные аспекты создания файла.</span><span class="sxs-lookup"><span data-stu-id="c1c83-119">The writer object handles all the other aspects of creating the file.</span></span>

<span data-ttu-id="c1c83-120">Выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c1c83-120">Perform the following steps:</span></span>

1.  <span data-ttu-id="c1c83-121">Создайте объект модуля записи, вызвав функцию [**вмкреатевритер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) , которая возвращает указатель [**ивмвритер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) .</span><span class="sxs-lookup"><span data-stu-id="c1c83-121">Create the writer object by calling the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function, which returns an [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) pointer.</span></span>
2.  <span data-ttu-id="c1c83-122">Создайте объект приемника push-уведомлений, вызвав функцию [**вмкреатевритерпушсинк**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) , которая возвращает указатель [**ивмвритерпушсинк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) .</span><span class="sxs-lookup"><span data-stu-id="c1c83-122">Create the push sink object by calling the [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) function, which returns an [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) pointer.</span></span>
3.  <span data-ttu-id="c1c83-123">Подключите сетевой приемник к модулю записи, вызвав [**ивмвритерадванцед:: аддсинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) в модуле записи, указав указатель на интерфейс **ивмвритерпушсинк** сетевого приемника.</span><span class="sxs-lookup"><span data-stu-id="c1c83-123">Attach the network sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) on the writer, with a pointer to the network sink's **IWMWriterPushSink** interface.</span></span>
4.  <span data-ttu-id="c1c83-124">Подключитесь к серверу, вызвав [**ивмвритерпушсинк:: Connect**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).</span><span class="sxs-lookup"><span data-stu-id="c1c83-124">Connect to the server by calling [**IWMWriterPushSink::Connect**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).</span></span>
5.  <span data-ttu-id="c1c83-125">запись потока;</span><span class="sxs-lookup"><span data-stu-id="c1c83-125">Write the stream.</span></span> <span data-ttu-id="c1c83-126">Этот шаг включает настройку профиля для объекта модуля записи, отправку образцов в модуль записи и, возможно, другие задачи.</span><span class="sxs-lookup"><span data-stu-id="c1c83-126">This step involves setting the profile on the writer object, sending samples to the writer, and possibly other tasks.</span></span> <span data-ttu-id="c1c83-127">Дополнительные сведения см. в разделе [запись файлов ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="c1c83-127">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span> <span data-ttu-id="c1c83-128">Дополнительные задачи могут включать в себя задание атрибутов метаданных (как описано в разделе [Работа с метаданными](working-with-metadata.md)) или задание динамического управления цифровыми правами (DRM) в потоке (как описано в разделе [Включение поддержки DRM](enabling-drm-support.md)).</span><span class="sxs-lookup"><span data-stu-id="c1c83-128">Additional tasks might include setting metadata attributes (as described in [Working with Metadata](working-with-metadata.md)) or setting live-DRM on the stream (as described in [Enabling DRM Support](enabling-drm-support.md)).</span></span> <span data-ttu-id="c1c83-129">Эти задачи выполняются в точности так же, как и для записи файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="c1c83-129">These tasks are performed exactly as they are for ASF file writing.</span></span>
6.  <span data-ttu-id="c1c83-130">После завершения записи вызовите [**ивмвритерадванцед:: ремовесинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) в модуле записи, чтобы отсоединить объект приемника Push.</span><span class="sxs-lookup"><span data-stu-id="c1c83-130">After you are done writing, call [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) on the writer to detach the push sink object.</span></span>
7.  <span data-ttu-id="c1c83-131">Вызовите [**ивмвритерпушсинк:: EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) в приемнике push-уведомлений, чтобы завершить сеанс с сервером.</span><span class="sxs-lookup"><span data-stu-id="c1c83-131">Call [**IWMWriterPushSink::EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) on the push sink to end the session with the server.</span></span>

<span data-ttu-id="c1c83-132">Эти шаги показаны в примере приложения Вмвнетврите.</span><span class="sxs-lookup"><span data-stu-id="c1c83-132">These steps are illustrated in the WMVNetWrite sample application.</span></span>

> [!Note]  
> <span data-ttu-id="c1c83-133">Если вы отправляете файл только для видео с очень низкими темпами, он может не начать играть на точке публикации в течение нескольких секунд.</span><span class="sxs-lookup"><span data-stu-id="c1c83-133">If you are sending a very-low-bit-rate video-only file, it might not start playing on the publishing point for several seconds.</span></span> <span data-ttu-id="c1c83-134">Это может произойти в различных случаях, например, когда один пакет содержит много мелких видеокадров и не имеет звукового сигнала, или если между первым пакетом и вторым пакетом в видеофайле с низким уровнем поразрядной скоростью существует длительный промежуток времени.</span><span class="sxs-lookup"><span data-stu-id="c1c83-134">This can happen in various cases, for example when a single packet contains many small video frames and no audio, or when there is a long time gap between the first packet and the second packet in a low-bit-rate video-only file.</span></span> <span data-ttu-id="c1c83-135">Чтобы избежать этой проблемы, вставьте в файл тихий аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="c1c83-135">To avoid this problem, insert a silent audio stream into the file.</span></span>

 

## <a name="authentication"></a><span data-ttu-id="c1c83-136">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="c1c83-136">Authentication</span></span>

<span data-ttu-id="c1c83-137">Проверка подлинности на сервере автоматически обрабатывается объектом извещающего приемника.</span><span class="sxs-lookup"><span data-stu-id="c1c83-137">Authentication to the server is automatically handled by the push sink object.</span></span> <span data-ttu-id="c1c83-138">Однако приложению может потребоваться предоставить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c1c83-138">However, the application may need to supply credentials.</span></span> <span data-ttu-id="c1c83-139">Это делается через интерфейс обратного вызова **ивмкредентиалкаллбакк** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="c1c83-139">This is done through the **IWMCredentialCallback** callback interface, as follows:</span></span>

1.  <span data-ttu-id="c1c83-140">Реализуйте интерфейс [**ивмстатускаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) и [**ивмкредентиалкаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) в приложении.</span><span class="sxs-lookup"><span data-stu-id="c1c83-140">Implement the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) and [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) interface in your application.</span></span>
2.  <span data-ttu-id="c1c83-141">Запросите объект приемника push-уведомлений для интерфейса [**ивмрегистеркаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="c1c83-141">Query the push sink object for the [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) interface.</span></span>
3.  <span data-ttu-id="c1c83-142">Вызовите [**ивмрегистеркаллбакк:: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) с указателем на интерфейс **ивмстатускаллбакк** вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="c1c83-142">Call [**IWMRegisterCallback::Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) with a pointer to your application's **IWMStatusCallback** interface.</span></span>
4.  <span data-ttu-id="c1c83-143">Если приемнику push-уведомлений необходимо получить учетные данные из приложения, он запрашивает **ивмстатускаллбаккный** указатель для интерфейса **Ивмкредентиалкаллбакк** и вызывает [**ивмкредентиалкаллбакк:: аккуирекредентиалс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials).</span><span class="sxs-lookup"><span data-stu-id="c1c83-143">If the push sink needs to get credentials from the application, it queries the **IWMStatusCallback** pointer for the **IWMCredentialCallback** interface and calls [**IWMCredentialCallback::AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials).</span></span> <span data-ttu-id="c1c83-144">Сведения об этом методе см. в разделе [Проверка подлинности](authentication.md).</span><span class="sxs-lookup"><span data-stu-id="c1c83-144">For information about this method, see [Authentication](authentication.md).</span></span>
5.  <span data-ttu-id="c1c83-145">По завершении вызовите [**ивмрегистеркаллбакк:: unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) , чтобы не получать уведомления о событиях из приемника push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c1c83-145">When you are done, call [**IWMRegisterCallback::Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) to stop getting event notifications from the push sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1c83-146">См. также</span><span class="sxs-lookup"><span data-stu-id="c1c83-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1c83-147">**Отправка данных ASF по сети**</span><span class="sxs-lookup"><span data-stu-id="c1c83-147">**Sending ASF Data Over a Network**</span></span>](sending-asf-data-over-a-network.md)
</dt> <dt>

[<span data-ttu-id="c1c83-148">**Работа с приемниками модуля записи**</span><span class="sxs-lookup"><span data-stu-id="c1c83-148">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> <dt>

[<span data-ttu-id="c1c83-149">**Объект приемника push-уведомлений**</span><span class="sxs-lookup"><span data-stu-id="c1c83-149">**Writer Push Sink Object**</span></span>](writer-push-sink-object.md)
</dt> </dl>

 

 




