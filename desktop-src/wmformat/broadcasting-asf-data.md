---
title: Трансляция данных ASF
description: Трансляция данных ASF
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows Media Format SDK, рассылка данных ASF
- Расширенный формат систем (ASF), данные вещания
- ASF (Расширенный системный формат), широковещательная рассылка данных
- Пакет SDK для Windows Media Format, отправка данных ASF
- Расширенный системный формат (ASF), отправка данных
- ASF (Расширенный системный формат), отправка данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42339b4a3e60666c1ea0cb69a07dfdc836b19409
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "104069679"
---
# <a name="broadcasting-asf-data"></a><span data-ttu-id="f363d-109">Трансляция данных ASF</span><span class="sxs-lookup"><span data-stu-id="f363d-109">Broadcasting ASF Data</span></span>

<span data-ttu-id="f363d-110">В этом разделе описывается отправка данных ASF по сети с помощью протокола HTTP.</span><span class="sxs-lookup"><span data-stu-id="f363d-110">This topic describes how to send ASF data across a network using the HTTP protocol.</span></span> <span data-ttu-id="f363d-111">Для отправки файлов по сети необходимо использовать объект модуля записи, поэтому прежде чем читать этот раздел, необходимо получить общее представление об этом объекте.</span><span class="sxs-lookup"><span data-stu-id="f363d-111">Sending files over a network requires the use of the writer object, so you should have a general understanding of this object before reading this topic.</span></span> <span data-ttu-id="f363d-112">Дополнительные сведения см. в разделе [запись файлов ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="f363d-112">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>

<span data-ttu-id="f363d-113">Если вы начинаете с несжатых данных, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f363d-113">If you are starting with uncompressed data, do the following:</span></span>

1.  <span data-ttu-id="f363d-114">Создайте объект модуля записи, вызвав функцию [**вмкреатевритер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) .</span><span class="sxs-lookup"><span data-stu-id="f363d-114">Create the writer object by calling the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="f363d-115">Эта функция возвращает указатель **ивмвритер** .</span><span class="sxs-lookup"><span data-stu-id="f363d-115">This function returns an **IWMWriter** pointer.</span></span>
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  <span data-ttu-id="f363d-116">Создайте объект приемника сети, вызвав функцию [**вмкреатевритернетворксинк**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) , которая возвращает указатель **ивмвритернетворксинк** .</span><span class="sxs-lookup"><span data-stu-id="f363d-116">Create the network sink object by calling the [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) function, which returns an **IWMWriterNetworkSink** pointer.</span></span>
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  <span data-ttu-id="f363d-117">Вызовите [**ивмвритернетворксинк:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) в сетевом приемнике и укажите номер порта, который нужно открыть; Например, 8080.</span><span class="sxs-lookup"><span data-stu-id="f363d-117">Call [**IWMWriterNetworkSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) on the network sink and specify the port number to open; for example, 8080.</span></span> <span data-ttu-id="f363d-118">При необходимости вызовите [**ивмвритернетворксинк:: жесостурл**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) , чтобы получить URL-адрес узла.</span><span class="sxs-lookup"><span data-stu-id="f363d-118">Optionally, call [**IWMWriterNetworkSink::GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) to get the URL of the host.</span></span> <span data-ttu-id="f363d-119">Клиенты будут обращаться к содержимому из этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f363d-119">Clients will access the content from this URL.</span></span> <span data-ttu-id="f363d-120">Можно также вызвать метод [**ивмвритернетворксинк:: сетмаксимумклиентс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) , чтобы ограничить количество клиентов.</span><span class="sxs-lookup"><span data-stu-id="f363d-120">You can also call [**IWMWriterNetworkSink::SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) to restrict the number of clients.</span></span>
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  <span data-ttu-id="f363d-121">Подключите сетевой приемник к модулю записи, вызвав [**ивмвритерадванцед:: аддсинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) в модуле записи, указав указатель на интерфейс **ивмвритернетворксинк** сетевого приемника.</span><span class="sxs-lookup"><span data-stu-id="f363d-121">Attach the network sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) on the writer, with a pointer to the network sink's **IWMWriterNetworkSink** interface.</span></span>
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  <span data-ttu-id="f363d-122">Задайте профиль ASF, вызвав метод [**ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) объекта Writer с указателем [**ивмпрофиле**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="f363d-122">Set the ASF profile by calling the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method on the writer object, with an [**IWMProfile**](iwmprofile.md) pointer.</span></span> <span data-ttu-id="f363d-123">Сведения о создании профиля см. в разделе [Работа с профилями](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="f363d-123">For information about creating a profile, see [Working with Profiles](working-with-profiles.md).</span></span>
6.  <span data-ttu-id="f363d-124">При необходимости укажите метаданные с помощью интерфейса [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) в модуле записи.</span><span class="sxs-lookup"><span data-stu-id="f363d-124">Optionally, specify metadata using the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface on the writer.</span></span>
7.  <span data-ttu-id="f363d-125">Вызовите [**ивмвритер:: бегинвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) в модуле записи.</span><span class="sxs-lookup"><span data-stu-id="f363d-125">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  <span data-ttu-id="f363d-126">Для каждого образца вызовите метод [**ивмвритер:: вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="f363d-126">For each sample, call the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span> <span data-ttu-id="f363d-127">Укажите номер потока, время презентации, длительность выборки и указатель на буфер выборки.</span><span class="sxs-lookup"><span data-stu-id="f363d-127">Specify the stream number, the presentation time, the duration of the sample, and a pointer to the sample buffer.</span></span> <span data-ttu-id="f363d-128">Метод **вритесампле** сжимает образцы.</span><span class="sxs-lookup"><span data-stu-id="f363d-128">The **WriteSample** method compresses the samples.</span></span>
9.  <span data-ttu-id="f363d-129">По завершении вызовите метод [**ивмвритер:: ендвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) в модуле записи.</span><span class="sxs-lookup"><span data-stu-id="f363d-129">When you are done, call [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. <span data-ttu-id="f363d-130">Вызовите [**ивмвритерадванцед:: ремовесинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) в модуле записи, чтобы отсоединить объект приемника сети.</span><span class="sxs-lookup"><span data-stu-id="f363d-130">Call [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) on the writer to detach the network sink object.</span></span>
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. <span data-ttu-id="f363d-131">Вызовите [**ивмвритернетворксинк:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) в сетевом приемнике, чтобы освободить порт.</span><span class="sxs-lookup"><span data-stu-id="f363d-131">Call [**IWMWriterNetworkSink::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) on the network sink to release the port.</span></span>
    ```C++
    hr = pNetSink->Close();
    ```

    

<span data-ttu-id="f363d-132">Другим способом потоковой передачи содержимого ASF по сети является его чтение из существующего ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="f363d-132">Another way to stream ASF content over a network is to read it from an existing ASF file.</span></span> <span data-ttu-id="f363d-133">Этот подход демонстрируется в примере Вмвнетврите, приведенном в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="f363d-133">The WMVNetWrite sample provided in the SDK demonstrates this approach.</span></span> <span data-ttu-id="f363d-134">В дополнение к приведенным выше шагам выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f363d-134">In addition to the steps listed previously, do the following:</span></span>

1.  <span data-ttu-id="f363d-135">Создайте объект Reader и вызовите метод **Open** с именем файла.</span><span class="sxs-lookup"><span data-stu-id="f363d-135">Create a reader object and call the **Open** method with the name of the file.</span></span>
2.  <span data-ttu-id="f363d-136">Вызовите [**ивмреадерадванцед:: сетмануалстреамселектион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) в объекте Reader со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="f363d-136">Call [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) on the reader object, with the value **TRUE**.</span></span> <span data-ttu-id="f363d-137">Это позволяет приложению считывать каждый поток в файле, включая потоки с взаимным исключением.</span><span class="sxs-lookup"><span data-stu-id="f363d-137">This enables the application to read every stream in the file, including streams with mutual exclusion.</span></span>
3.  <span data-ttu-id="f363d-138">Запросите средство чтения для интерфейса [**ивмпрофиле**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="f363d-138">Query the reader for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="f363d-139">Этот указатель используется при вызове [**ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) в объекте модуля записи (шаг 5 в предыдущей процедуре).</span><span class="sxs-lookup"><span data-stu-id="f363d-139">Use this pointer when you call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) on the writer object (step 5 in the previous procedure).</span></span>
4.  <span data-ttu-id="f363d-140">Для каждого потока, определенного в профиле, вызовите [**ивмпрофиле:: Stream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) , чтобы получить номер потока.</span><span class="sxs-lookup"><span data-stu-id="f363d-140">For every stream defined in the profile, call [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) to get the stream number.</span></span> <span data-ttu-id="f363d-141">Передайте этот номер потока в метод [**ивмреадерадванцед:: сетрецеивестреамсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) средства чтения.</span><span class="sxs-lookup"><span data-stu-id="f363d-141">Pass this stream number to the reader's [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) method.</span></span> <span data-ttu-id="f363d-142">Этот метод информирует читателя о необходимости доставки сжатых образцов, а не декодирования их.</span><span class="sxs-lookup"><span data-stu-id="f363d-142">This method informs the reader to deliver compressed samples, rather than decoding them.</span></span> <span data-ttu-id="f363d-143">Образцы будут доставляться в приложение с помощью метода обратного вызова [**ивмреадеркаллбаккадванцед:: онстреамсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) приложения.</span><span class="sxs-lookup"><span data-stu-id="f363d-143">The samples will be delivered to the application through the application's [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span>

    <span data-ttu-id="f363d-144">Необходимо получить сведения о кодека для каждого потока, который вы читаете без сжатия, и добавить его в заголовок перед рассылкой.</span><span class="sxs-lookup"><span data-stu-id="f363d-144">You must obtain codec information for every stream that you read uncompressed and add it to the header before broadcast.</span></span> <span data-ttu-id="f363d-145">Чтобы получить сведения о кодека, вызовите [**IWMHeaderInfo2:: жеткодеЦинфокаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) и [**IWMHeaderInfo2:: жеткодеЦинфо**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) , чтобы перечислить кодеки, связанные с файлом, в модуле чтения.</span><span class="sxs-lookup"><span data-stu-id="f363d-145">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="f363d-146">Выберите сведения о кодека, соответствующие конфигурации потока.</span><span class="sxs-lookup"><span data-stu-id="f363d-146">Select the codec information that matches the stream configuration.</span></span> <span data-ttu-id="f363d-147">Затем задайте сведения о кодека в средстве записи, вызвав [**IWMHeaderInfo3:: аддкодеЦинфо**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), передав данные, полученные от модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="f363d-147">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

5.  <span data-ttu-id="f363d-148">После настройки профиля в модуле записи вызовите [**ивмвритер:: жетинпуткаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) в модуле записи, чтобы получить число входов.</span><span class="sxs-lookup"><span data-stu-id="f363d-148">After you set the profile on the writer, call [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) on the writer to get the number of inputs.</span></span> <span data-ttu-id="f363d-149">Для каждого входа вызовите [**ивмвритер:: сетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) со значением **null**.</span><span class="sxs-lookup"><span data-stu-id="f363d-149">For each input, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) with the value **NULL**.</span></span> <span data-ttu-id="f363d-150">Это указывает объекту модуля записи, что приложение будет доставлять сжатые образцы, поэтому модуль записи не должен использовать ни один кодек для сжатия данных.</span><span class="sxs-lookup"><span data-stu-id="f363d-150">This indicates to the writer object that the application will deliver compressed samples, so the writer does not have to use any codecs to compress the data.</span></span> <span data-ttu-id="f363d-151">Перед вызовом **бегинвритинг** необходимо вызвать метод **сетинпутпропс** .</span><span class="sxs-lookup"><span data-stu-id="f363d-151">Make sure to call **SetInputProps** before calling **BeginWriting**.</span></span>
6.  <span data-ttu-id="f363d-152">При необходимости скопируйте атрибуты метаданных из модуля чтения в модуль записи</span><span class="sxs-lookup"><span data-stu-id="f363d-152">Optionally, copy the metadata attributes from the reader to the writer</span></span>
7.  <span data-ttu-id="f363d-153">Поскольку образцы из модуля чтения уже сжаты, используйте метод [**ивмвритерадванцед:: вритестреамсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) для записи образцов вместо метода **вритесампле** .</span><span class="sxs-lookup"><span data-stu-id="f363d-153">Because the samples from the reader are already compressed, use the [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) method to write the samples, instead of the **WriteSample** method.</span></span> <span data-ttu-id="f363d-154">Метод **вритестреамсампле** обходит обычные процедуры сжатия объекта модуля записи.</span><span class="sxs-lookup"><span data-stu-id="f363d-154">The **WriteStreamSample** method bypasses the writer object's usual compression procedures.</span></span>
8.  <span data-ttu-id="f363d-155">Когда модуль чтения достигнет конца файла, он отправляет \_ приложению уведомление ВМТ EOF.</span><span class="sxs-lookup"><span data-stu-id="f363d-155">When the reader reaches the end of the file, it sends a WMT\_EOF notification to the application.</span></span>

<span data-ttu-id="f363d-156">Кроме того, приложение должно запрашивать часы на объекте модуля чтения, чтобы средство чтения запрашивает данные из файла как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="f363d-156">In addition, the application should drive the clock on the reader object, so that the reader pulls data from the file as quickly as possible.</span></span> <span data-ttu-id="f363d-157">Для этого вызовите метод [**ивмреадерадванцед:: сетусерпровидедклокк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) в средстве чтения со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="f363d-157">To do this, call the [**IWMReaderAdvanced::SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) method on the reader, with the value **TRUE**.</span></span> <span data-ttu-id="f363d-158">После того как модуль чтения отправит \_ уведомление Started ВМТ, вызовите [**ивмреадерадванцед::D еливертиме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) и укажите интервал времени, который должен доставлять модуль чтения.</span><span class="sxs-lookup"><span data-stu-id="f363d-158">After the reader sends the WMT\_STARTED notification, call [**IWMReaderAdvanced::DeliverTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) and specify the time interval that the reader should deliver.</span></span> <span data-ttu-id="f363d-159">После того, как модуль чтения прочитает этот интервал времени, он вызывает метод обратного вызова [**ивмреадеркаллбаккадванцед:: OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) приложения.</span><span class="sxs-lookup"><span data-stu-id="f363d-159">After the reader is done reading this time interval, it calls the application's [**IWMReaderCallbackAdvanced::OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) callback method.</span></span> <span data-ttu-id="f363d-160">Приложение должно вызвать **деливертиме** еще раз для чтения следующего интервала времени.</span><span class="sxs-lookup"><span data-stu-id="f363d-160">The application should call **DeliverTime** again to read the next time interval.</span></span> <span data-ttu-id="f363d-161">Например, для чтения из файла с интервалом в одну секунду:</span><span class="sxs-lookup"><span data-stu-id="f363d-161">For example, to read from the file in one-second intervals:</span></span>


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="f363d-162">См. также</span><span class="sxs-lookup"><span data-stu-id="f363d-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f363d-163">**Отправка данных ASF по сети**</span><span class="sxs-lookup"><span data-stu-id="f363d-163">**Sending ASF Data Over a Network**</span></span>](sending-asf-data-over-a-network.md)
</dt> <dt>

[<span data-ttu-id="f363d-164">**Работа с приемниками модуля записи**</span><span class="sxs-lookup"><span data-stu-id="f363d-164">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




