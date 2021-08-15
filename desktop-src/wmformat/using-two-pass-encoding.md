---
title: использование кодировки Two-Pass (пакет SDK для Windows Media Format 11)
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
ms.openlocfilehash: fd0683af636197b3f8116fca4dea85ce15609d2c99b0d9e0c11dfe0a2662a424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653839"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a>использование кодировки Two-Pass (пакет SDK для Windows Media Format 11)

Некоторые кодеки поддерживают двустороннюю кодировку для определенных форматов. В некоторых случаях кодек требует, чтобы указанный формат был закодирован с помощью двух проходов. При использовании двух-проходного кодирования перед началом кодирования вы отправляете образцы потока в кодек. Кодек анализирует образцы и настраивает проход кодирования на основе анализа. Это приводит к более эффективному кодированию файла.

Чтобы определить, поддерживает ли кодек однопроходную кодировку (или два прохода или оба) для определенного формата, вызовите [**IWMCodecInfo3:: сеткодеценумератионсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) с g \_ всзнумпассес и соответствующим значением, а затем перечислите форматы, чтобы убедиться, что возвращается нужный. дополнительные сведения о кодеках Windows Media, поддерживающих двустороннюю кодировку, см. в разделе [выбор метода кодирования](choosing-an-encoding-method.md).

вы можете использовать двустороннюю кодировку с пакетом SDK для Windows Media Format, вызвав методы интерфейса [**ивмвритерпрепроцесс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) .

В случаях, когда для определенного формата требуется многопроходная кодировка, но приложению не удается выполнить этап предварительной обработки, первый вызов [**вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) завершится сбоем с \_ \_ недопустимым \_ числом входов в NS E \_ .

В следующем примере функции показано, как выполнить двустороннюю кодировку. Эта функция вызывается после настройки модуля записи с помощью профиля и запуска. Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Запись файлов ASF**](writing-asf-files.md)
</dt> </dl>

 

 




