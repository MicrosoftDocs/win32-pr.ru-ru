---
title: Использование кодировки Two-Pass (пакет SDK для формата Windows Media 11)
description: Использование кодировки Two-Pass
ms.assetid: 55fc768b-15f0-4236-ad0d-3792ccaa9b4f
keywords:
- Расширенный формат систем (ASF), два прохода кодирования
- ASF (Расширенный системный формат), 2-проходная кодировка
- 2-проходная кодировка, о
- 2. Передача кодирования, сведения
- кодеки, два прохода кодирования
- многопроходная кодировка, интерфейс Ивмвритерпрепроцесс
- 2. передача кодировки, интерфейс Ивмвритерпрепроцесс
- ивмвритерпрепроцесс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3794856f47c1656cc53006268c41a063cdde96
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533722"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a><span data-ttu-id="03d93-111">Использование кодировки Two-Pass (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="03d93-111">Using Two-Pass Encoding (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="03d93-112">Некоторые кодеки поддерживают двустороннюю кодировку для определенных форматов.</span><span class="sxs-lookup"><span data-stu-id="03d93-112">Some codecs support two-pass encoding for certain formats.</span></span> <span data-ttu-id="03d93-113">В некоторых случаях кодек требует, чтобы указанный формат был закодирован с помощью двух проходов.</span><span class="sxs-lookup"><span data-stu-id="03d93-113">In some cases, a codec requires that a specified format be encoded using two passes.</span></span> <span data-ttu-id="03d93-114">При использовании двух-проходного кодирования перед началом кодирования вы отправляете образцы потока в кодек.</span><span class="sxs-lookup"><span data-stu-id="03d93-114">When two-pass encoding is used, you send the samples for the stream to the codec before the encoding pass.</span></span> <span data-ttu-id="03d93-115">Кодек анализирует образцы и настраивает проход кодирования на основе анализа.</span><span class="sxs-lookup"><span data-stu-id="03d93-115">The codec analyzes the samples and configures the encoding pass based on the analysis.</span></span> <span data-ttu-id="03d93-116">Это приводит к более эффективному кодированию файла.</span><span class="sxs-lookup"><span data-stu-id="03d93-116">This results in a more efficiently encoded file.</span></span>

<span data-ttu-id="03d93-117">Чтобы определить, поддерживает ли кодек однопроходную кодировку (или два прохода или оба) для определенного формата, вызовите [**IWMCodecInfo3:: сеткодеценумератионсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) с g \_ всзнумпассес и соответствующим значением, а затем перечислите форматы, чтобы убедиться, что возвращается нужный.</span><span class="sxs-lookup"><span data-stu-id="03d93-117">To determine whether a codec supports one-pass encoding, or two-pass, or both, for a given format, call [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) with g\_wszNumPasses and the appropriate value, and then enumerate the formats to see if the one you want is returned.</span></span> <span data-ttu-id="03d93-118">Дополнительные сведения о кодеках Windows Media, поддерживающих двустороннюю кодировку, см. [в разделе Выбор метода кодирования](choosing-an-encoding-method.md).</span><span class="sxs-lookup"><span data-stu-id="03d93-118">For more information about the Windows Media codecs that support two-pass encoding, see [Choosing an Encoding Method](choosing-an-encoding-method.md).</span></span>

<span data-ttu-id="03d93-119">Можно использовать двустороннюю кодировку с пакетом SDK для формата Windows Media, вызывая методы интерфейса [**ивмвритерпрепроцесс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="03d93-119">You can use two-pass encoding with the Windows Media Format SDK by calling methods of the [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) interface.</span></span>

<span data-ttu-id="03d93-120">В случаях, когда для определенного формата требуется многопроходная кодировка, но приложению не удается выполнить этап предварительной обработки, первый вызов [**вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) завершится сбоем с \_ \_ недопустимым \_ числом входов в NS E \_ .</span><span class="sxs-lookup"><span data-stu-id="03d93-120">In cases where two-pass encoding is required for a particular format, but the application fails to perform a preprocessing pass, the first call to [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) will fail with NS\_E\_INVALID\_NUM\_PASSES.</span></span>

<span data-ttu-id="03d93-121">В следующем примере функции показано, как выполнить двустороннюю кодировку.</span><span class="sxs-lookup"><span data-stu-id="03d93-121">The following example function demonstrates how to perform two-pass encoding.</span></span> <span data-ttu-id="03d93-122">Эта функция вызывается после настройки модуля записи с помощью профиля и запуска.</span><span class="sxs-lookup"><span data-stu-id="03d93-122">This function is called after the writer has been set with a profile and started.</span></span> <span data-ttu-id="03d93-123">Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="03d93-123">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT PreProcess(IWMWriter* pWriter, DWORD dwInputNum)
{
    HRESULT hr        = S_OK;
    DWORD   dwMaxPass = 0;

    IWMWriterPreprocess* pPreProc = NULL;

    // Get the writer preprocessor interface.
    hr = pWriter->QueryInterface(IID_IWMWriterPreprocess, 
                                 (void**) &pPreProc);
    GOTO_EXIT_IF_FAILED(hr);

    // Check that the input can be preprocessed.
    hr = pPreProc->GetMaxPreprocessingPasses(dwInputNum,0, &dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    if(dwMaxPass == 0)
    {
        hr = NS_E_INVALID_REQUEST;
        goto Exit;
    }

    // Set the number of preprocessing passes to the maximum.
    hr = pPreProc->SetNumPreprocessingPasses(dwInputNum, 0, dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    // Call BeginWriting before calling BeginPreprocessingPass
    hr = pWriter->BeginWriting();

    // Start preprocessing the first pass.
    hr = pPreProc->BeginPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: Make repeated calls to pPreProc->PreprocessSample to
    // preprocess all the samples in the stream.

    // End preprocessing.
    hr = pPreProc->EndPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: If the maximum number of preprocessing passes is greater
    // than one, repeat the preprocessing steps for each pass.

Exit:
    SAFE_RELEASE(pPreProc);
    Return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="03d93-124">См. также</span><span class="sxs-lookup"><span data-stu-id="03d93-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03d93-125">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="03d93-125">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




