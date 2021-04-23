---
title: Расшифровка аудио в S/PDIF
description: Расшифровка аудио в S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- Windows Media Format SDK, декодирование аудио в S/PDIF
- Windows Media Format SDK, формат цифрового соединения Sony/Philips (S/PDIF)
- Расширенный системный формат (ASF), декодирование аудио в S/PDIF
- ASF (Расширенный системный формат), декодирование аудио в S/PDIF
- Формат ASF, Sony/Philips Digital Interconnect Format (S/PDIF)
- ASF (расширенный формат систем), формат цифровых соединений Sony/Philips (S/PDIF)
- Формат цифровых соединений Sony/Philips (S/PDIF), декодирование аудио
- S/PDIF (формат цифрового соединения Sony/Philips), декодирование аудио
- декодирование аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa063baa8e9a88c2fb7a4d9c67375965282167
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789223"
---
# <a name="to-decode-audio-to-spdif"></a><span data-ttu-id="c0ccd-112">Расшифровка аудио в S/PDIF</span><span class="sxs-lookup"><span data-stu-id="c0ccd-112">To Decode Audio to S/PDIF</span></span>

<span data-ttu-id="c0ccd-113">Звук, закодированный с помощью кодека Windows Media Audio 9 Professional, можно декодировать в формат Digital Interconnect (S/PDIF) Sony/Philips.</span><span class="sxs-lookup"><span data-stu-id="c0ccd-113">Audio encoded with the Windows Media Audio 9 Professional codec can be decoded to Sony/Philips Digital Interconnect Format (S/PDIF).</span></span> <span data-ttu-id="c0ccd-114">Чтобы создать выходные данные S/PDIF, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c0ccd-114">To generate S/PDIF output, perform the following steps:</span></span>

1.  <span data-ttu-id="c0ccd-115">Откройте файл, содержащий поток Windows Media Audio 9 Professional, вызвав метод [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .</span><span class="sxs-lookup"><span data-stu-id="c0ccd-115">Open a file that contains a Windows Media Audio 9 Professional stream by calling the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span>
2.  <span data-ttu-id="c0ccd-116">Найдите выходной номер нужного потока.</span><span class="sxs-lookup"><span data-stu-id="c0ccd-116">Identify the output number of the stream that you want.</span></span> <span data-ttu-id="c0ccd-117">Дополнительные сведения см. [в разделе чтобы определить выходные номера](to-identify-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="c0ccd-117">For more information, see [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="c0ccd-118">Вызовите метод [**IWMReaderAdvanced2:: сетаутпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) , чтобы настроить выходные данные S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="c0ccd-118">Call the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method to configure S/PDIF output.</span></span> <span data-ttu-id="c0ccd-119">Используйте g \_ всзенаблевмапроспдифаутпут для имени параметра.</span><span class="sxs-lookup"><span data-stu-id="c0ccd-119">Use g\_wszEnableWMAProSPDIFOutput for the setting name.</span></span> <span data-ttu-id="c0ccd-120">Тип данных — **ВМТ \_ типа \_ bool**; установите значение **true** , чтобы включить выходные данные S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="c0ccd-120">The data type is **WMT\_TYPE\_BOOL**; set the value to **TRUE** to enable S/PDIF output.</span></span>
4.  <span data-ttu-id="c0ccd-121">Получите интерфейс выходных свойств ([**ивмаутпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) требуемого формата выходных данных, вызвав метод [**Ивмреадер:: жетаутпутформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) .</span><span class="sxs-lookup"><span data-stu-id="c0ccd-121">Get the output properties interface ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) of the desired output format by calling the [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) method.</span></span> <span data-ttu-id="c0ccd-122">Дополнительные сведения о перечислении выходных форматов см. в разделе [назначение выходных форматов](assigning-output-formats.md).</span><span class="sxs-lookup"><span data-stu-id="c0ccd-122">For more information about enumerating output formats, see [Assigning Output Formats](assigning-output-formats.md).</span></span>
5.  <span data-ttu-id="c0ccd-123">Задайте формат вывода, вызвав метод [**ивмреадер:: сетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) .</span><span class="sxs-lookup"><span data-stu-id="c0ccd-123">Set the output format by calling the [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) method.</span></span> <span data-ttu-id="c0ccd-124">Передайте указатель на интерфейс **ивмаутпутмедиапропс** , полученный на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="c0ccd-124">Pass in a pointer to the **IWMOutputMediaProps** interface obtained in step 4.</span></span>
6.  <span data-ttu-id="c0ccd-125">Внесите любые другие изменения в конфигурацию и начните воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="c0ccd-125">Make any other configuration changes and begin playback.</span></span>

> [!Note]  
> <span data-ttu-id="c0ccd-126">Вы можете выполнить описанные выше действия в синхронном модуле чтения, используя соответствующие методы интерфейса [**ивмсинкреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .</span><span class="sxs-lookup"><span data-stu-id="c0ccd-126">You can perform the preceding steps on the synchronous reader by using the corresponding methods of the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

 

<span data-ttu-id="c0ccd-127">В следующем примере кода показано, как настроить поток звука для вывода звука в виде данных S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="c0ccd-127">The following example code demonstrates how to set an audio stream to output audio as S/PDIF data.</span></span> <span data-ttu-id="c0ccd-128">Эта функция предполагает, что файл уже загружен в модуль чтения и был идентифицирован выходной номер.</span><span class="sxs-lookup"><span data-stu-id="c0ccd-128">This function assumes that a file has already been loaded in the reader and that the output number has been identified.</span></span> <span data-ttu-id="c0ccd-129">Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="c0ccd-129">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT SetSPDIF(DWORD dwOutputNum, IWMReader* pReader)
{
    HRESULT hr = S_OK;

    IWMReaderAdvanced2*  pReaderAdv   = NULL;
    IWMOutputMediaProps* pOutputProps = NULL; 

    BOOL fValue = TRUE;

    // Get the advanced reader interface.
    hr = pReader->QueryInterface(IID_IWMReaderAdvanced2,
                                 (void**)&pReaderAdv);
    GOTO_EXIT_IF_FAILED(hr);

    // Set S/PDIF output.
    hr = pReaderAdv->SetOutputSetting(dwOutputNum, 
                                      g_wszEnableWMAProSPDIFOutput, 
                                      WMT_TYPE_BOOL, 
                                      (BYTE*)&fValue, 
                                      sizeof(BOOL));
    GOTO_EXIT_IF_FAILED(hr);

    // Get the first output format for the stream.
    // NOTE: You could also enumerate the available output formats
    // and pick one to use.

    hr = pReader->GetOutputFormat(dwOutputNum, 0, &pOutputProps);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the output properties back on the reader.
    hr = pReader->SetOutputProps(dwOutputNum, pOutputProps);

Exit:
    SAFE_RELEASE(pReaderAdv);
    SAFE_RELEASE(pOutputProps);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c0ccd-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c0ccd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0ccd-131">**Дополнительные разделы**</span><span class="sxs-lookup"><span data-stu-id="c0ccd-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="c0ccd-132">**Чтение файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="c0ccd-132">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="c0ccd-133">**Интерфейс Ивмреадер**</span><span class="sxs-lookup"><span data-stu-id="c0ccd-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="c0ccd-134">**Интерфейс IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="c0ccd-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="c0ccd-135">**Интерфейс Ивмсинкреадер**</span><span class="sxs-lookup"><span data-stu-id="c0ccd-135">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




